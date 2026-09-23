# Hands-on L6: Report

**Name:**
**Student ID:**
**Email:**

---

## Seed and commands

Seed used for `datagen.py`:

The commands you ran, in order. If you deviated from the steps in the README, say where and
why.

```bash

```

---

## Results

For each task, the first ten rows of your output (from the terminal or the CSV file) and one
or two sentences on what they say about your data.

### Task 1: favorite genre per user

```
user_id,genre,play_count
user_1,Pop,6
user_10,Jazz,10
user_100,Jazz,7
user_11,Jazz,8
user_12,Jazz,9
user_13,Jazz,8
user_14,Hip-Hop,7
user_15,Pop,6
user_16,Hip-Hop,10
user_17,Jazz,8


```
These results show the favorite genre of each user. Jazz seems to be one of the more popular ones.


### Task 2: average listening time per song

```

song_id,title,avg_duration_sec,play_count
song_39,Title_song_39,201.38,21
song_12,Title_song_12,200.17,29
song_33,Title_song_33,197.38,29
song_2,Title_song_2,190.72,18
song_41,Title_song_41,187.8,15
song_19,Title_song_19,184.24,17
song_20,Title_song_20,183.8,20
song_23,Title_song_23,182.44,25
song_44,Title_song_44,181.14,29
song_29,Title_song_29,179.55,20

```
These results listed are the average listening time for each song. Song 39 is the highest.


### Task 3: genre loyalty score, top 10
```
user_id,genre,play_count,total_plays,loyalty_score
user_34,Pop,10,10,1.0
user_68,Pop,9,9,1.0
user_48,Jazz,8,8,1.0
user_36,Rock,5,5,1.0
user_84,Hip-Hop,4,4,1.0
user_53,Hip-Hop,16,17,0.941
user_30,Jazz,8,9,0.889
user_73,Pop,8,9,0.889
user_14,Hip-Hop,7,8,0.875
user_25,Classical,7,8,0.875





```

Why do users with few plays tend to get a score of 1.0? Would you change the definition of
the score to account for that?

users loyalty score of 1.0 can be achieved by listening to only one genre. Maybe adding a multiple loyalty scores for different ranges of listens would be better.

### Task 4: night owls

```
user_id,night_plays
user_51,6
user_19,5
user_27,5
user_76,5
user_8,5
user_21,4
user_22,4
user_6,4
user_61,4
user_67,4

```

Users listened to music the most at the night. User 51 had the most night listens.

---

## The plan

Paste the `explain()` output of task 1:

```
== Physical Plan ==
AdaptiveSparkPlan isFinalPlan=false
+- Sort [user_id#0 ASC NULLS FIRST], true, 0
   +- Exchange rangepartitioning(user_id#0 ASC NULLS FIRST, 200), ENSURE_REQUIREMENTS, [plan_id=975]
      +- Project [user_id#0, genre#7, play_count#28L]
         +- Filter (row#38 = 1)
            +- Window [row_number() windowspecdefinition(user_id#0, play_count#28L DESC NULLS LAST, genre#7 ASC NULLS FIRST, specifiedwindowframe(RowFrame, unboundedpreceding$(), currentrow$())) AS row#38], [user_id#0], [play_count#28L DESC NULLS LAST, genre#7 ASC NULLS FIRST]
               +- WindowGroupLimit [user_id#0], [play_count#28L DESC NULLS LAST, genre#7 ASC NULLS FIRST], row_number(), 1, Final
                  +- Sort [user_id#0 ASC NULLS FIRST, play_count#28L DESC NULLS LAST, genre#7 ASC NULLS FIRST], false, 0
                     +- Exchange hashpartitioning(user_id#0, 200), ENSURE_REQUIREMENTS, [plan_id=968]
                        +- WindowGroupLimit [user_id#0], [play_count#28L DESC NULLS LAST, genre#7 ASC NULLS FIRST], row_number(), 1, Partial
                           +- Sort [user_id#0 ASC NULLS FIRST, play_count#28L DESC NULLS LAST, genre#7 ASC NULLS FIRST], false, 0
                              +- HashAggregate(keys=[user_id#0, genre#7], functions=[count(1)])
                                 +- Exchange hashpartitioning(user_id#0, genre#7, 200), ENSURE_REQUIREMENTS, [plan_id=962]
                                    +- HashAggregate(keys=[user_id#0, genre#7], functions=[partial_count(1)])
                                       +- Project [user_id#0, genre#7]
                                          +- BroadcastHashJoin [song_id#1], [song_id#4], Inner, BuildRight, false, false
                                             :- Filter isnotnull(song_id#1)
                                             :  +- FileScan csv [user_id#0,song_id#1] Batched: false, DataFilters: [isnotnull(song_id#1)], Format: CSV, Location: InMemoryFileIndex(1 paths)[file:/opt/spark/work-dir/shared/input/listening_logs.csv], PartitionFilters: [], PushedFilters: [IsNotNull(song_id)], ReadSchema: struct<user_id:string,song_id:string>
                                             +- BroadcastExchange HashedRelationBroadcastMode(List(input[0, string, false]),false), [plan_id=957]
                                                +- Filter isnotnull(song_id#4)
                                                   +- FileScan csv [song_id#4,genre#7] Batched: false, DataFilters: [isnotnull(song_id#4)], Format: CSV, Location: InMemoryFileIndex(1 paths)[file:/opt/spark/work-dir/shared/input/songs_metadata.csv], PartitionFilters: [], PushedFilters: [IsNotNull(song_id)], ReadSchema: struct<song_id:string,genre:string>



```

Your reading of it: where are the two file scans, which operator is the join and which kind
of join did Spark choose, where are the shuffles (`Exchange`) and why are they needed, and
how does this match the diagram in the SQL / DataFrame tab of the Spark UI?

The filescan operators reads listening_logs.csv and songs_metadata.csv. Spark uses the BroadcastHashJoin, and the Exchange operators for shuffling the data, grouping, windowing and final sorting

---

## Transformations and actions

Which lines of your `main.py` are actions? How many jobs did the program launch according to
the Spark UI, and is that what you expected?

My programed launched 40 jobs. It can be expected since one spark job can make others.

---

## Problems and fixes

Anything that went wrong and what resolved it. Paste the actual error message. If nothing
went wrong, say so.


nothing went wrong
