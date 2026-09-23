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
user_18,Rock,8
user_19,Jazz,5
user_2,Jazz,5
user_20,Classical,4
user_21,Jazz,8
user_22,Jazz,5
user_23,Jazz,5
user_24,Classical,9
user_25,Classical,7
user_26,Pop,9
user_27,Classical,13
user_28,Jazz,3
user_29,Hip-Hop,9
user_3,Hip-Hop,2
user_30,Jazz,8
user_31,Rock,6
user_32,Jazz,10
user_33,Jazz,8
user_34,Pop,10
user_35,Classical,7
user_36,Rock,5
user_37,Hip-Hop,4
user_38,Hip-Hop,7
user_39,Classical,6
user_4,Classical,12
user_40,Rock,12
user_41,Rock,8
user_42,Pop,14
user_43,Pop,9
user_44,Hip-Hop,7
user_45,Rock,6
user_46,Hip-Hop,5
user_47,Classical,7
user_48,Jazz,8
user_49,Hip-Hop,6
user_5,Pop,6
user_50,Classical,6
user_51,Pop,8
user_52,Hip-Hop,8
user_53,Hip-Hop,16
user_54,Hip-Hop,6
user_55,Jazz,3
user_56,Jazz,5
user_57,Pop,7
user_58,Pop,4
user_59,Rock,7
user_6,Classical,8
user_60,Hip-Hop,6
user_61,Rock,5
user_62,Hip-Hop,5
user_63,Rock,5
user_64,Rock,5
user_65,Hip-Hop,4
user_66,Hip-Hop,4
user_67,Classical,15
user_68,Pop,9
user_69,Classical,6
user_7,Hip-Hop,6
user_70,Jazz,9
user_71,Pop,7
user_72,Pop,9
user_73,Pop,8
user_74,Hip-Hop,5
user_75,Classical,3
user_76,Pop,13
user_77,Pop,9
user_78,Hip-Hop,2
user_79,Jazz,2
user_8,Hip-Hop,7
user_80,Hip-Hop,4
user_81,Hip-Hop,6
user_82,Classical,5
user_83,Classical,3
user_84,Hip-Hop,4
user_85,Hip-Hop,8
user_86,Pop,5
user_87,Hip-Hop,3
user_88,Classical,2
user_89,Hip-Hop,7
user_9,Jazz,6
user_90,Pop,5
user_91,Hip-Hop,6
user_92,Jazz,7
user_93,Jazz,5
user_94,Classical,12
user_95,Pop,5
user_96,Jazz,13
user_97,Pop,4
user_98,Classical,4
user_99,Pop,4

These results show the favorite genre of each user. Jazz seems to be one of the more popular ones.

```

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
song_48,Title_song_48,178.69,16
song_8,Title_song_8,178.04,27
song_50,Title_song_50,175.54,26
song_47,Title_song_47,175.33,33
song_35,Title_song_35,174.41,22
song_9,Title_song_9,173.4,15
song_31,Title_song_31,173.16,19
song_38,Title_song_38,172.63,27
song_22,Title_song_22,171.76,17
song_4,Title_song_4,166.62,13
song_5,Title_song_5,166.4,15
song_27,Title_song_27,166.24,17
song_6,Title_song_6,165.05,21
song_16,Title_song_16,164.13,16
song_17,Title_song_17,163.43,14
song_7,Title_song_7,162.61,23
song_46,Title_song_46,160.24,17
song_42,Title_song_42,158.41,17
song_14,Title_song_14,158.32,34
song_1,Title_song_1,157.38,29
song_21,Title_song_21,156.62,21
song_10,Title_song_10,156.52,23
song_32,Title_song_32,154.47,17
song_26,Title_song_26,153.47,17
song_40,Title_song_40,153.37,30
song_49,Title_song_49,152.89,19
song_30,Title_song_30,151.8,25
song_45,Title_song_45,151.18,17
song_24,Title_song_24,151.1,20
song_13,Title_song_13,150.33,12
song_43,Title_song_43,149.37,19
song_15,Title_song_15,148.69,13
song_36,Title_song_36,144.91,11
song_25,Title_song_25,144.71,14
song_11,Title_song_11,143.69,13
song_37,Title_song_37,142.82,17
song_3,Title_song_3,132.32,25
song_28,Title_song_28,131.22,18
song_34,Title_song_34,122.5,18
song_18,Title_song_18,104.7,10


These results listed are the average listening time for each song. Song 39 is the highest.

```

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


users loyalty score of 1.0 can be achieved by listening to only one genre. Maybe adding a multiple loyalty scores for different ranges of listens would be better.


```

Why do users with few plays tend to get a score of 1.0? Would you change the definition of
the score to account for that?

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
user_81,4
user_91,4
user_1,3
user_23,3
user_28,3
user_33,3
user_4,3
user_50,3
user_53,3
user_57,3
user_59,3
user_60,3
user_68,3
user_71,3
user_77,3
user_80,3
user_85,3
user_88,3
user_93,3
user_95,3
user_10,2
user_12,2
user_16,2
user_25,2
user_30,2
user_32,2
user_39,2
user_41,2
user_42,2
user_44,2
user_45,2
user_48,2
user_5,2
user_54,2
user_58,2
user_64,2
user_66,2
user_70,2
user_72,2
user_79,2
user_89,2
user_97,2
user_100,1
user_11,1
user_14,1
user_15,1
user_17,1
user_2,1
user_24,1
user_29,1
user_34,1
user_35,1
user_36,1
user_38,1
user_40,1
user_43,1
user_46,1
user_49,1
user_52,1
user_55,1
user_56,1
user_62,1
user_63,1
user_65,1
user_69,1
user_7,1
user_73,1
user_74,1
user_75,1
user_78,1
user_82,1
user_83,1
user_9,1
user_90,1
user_92,1
user_94,1
user_96,1
user_98,1
user_99,1

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
