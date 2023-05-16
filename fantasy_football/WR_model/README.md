# Clustering NFL Wide Receivers to Improve Fantasy Football Rookie Draft Outcomes

## Table of Contents
* [Installation](#Installation)
* [Project Motivation and Description](#motivation)
* [File Description](#description)
* [Results](#Results)


## Installation
The code requires Python versions of 3.* as well as the following modules:
* pandas
* numpy
* matplotlib.pyplot
* seaborn as sns
* math


## Project Objective and Description <a name="motivation"></a>
The objective of this project is to use k-means unsupervised learning to cluster similar NFL wide receivers together in an attempt to improve fantasy football rookie draft decisions. The model is built using data involving players' NCAA stats and NFL combine data. The features and their descriptions are below:

Feature Description:
* DP: draft pick where player was selected in the NFL draft
* REC_per_GP: receptions per game
* REC_Yards_per_GP: receiving yards per game
* REC_TDs_per_GP: receiving touchdowns per game
* Yards_per_REC: yards gained per receptions
* Touches_per_GP: touches per game
* PPR_per_GP: average fantasy points per game (PPR style scoring) in college
* Combined_REC_MS: a metric designed to represent a player's receiving production in their college offense
* RecPTMPA: receptions per team pass attempt
* REC_Yards_per_TM_PA: receiving yards per team pass attempt
* REC_TDS_per_TM_PA: receiving touchdowns per team pass attempt
* REC_CD: represents the player's percentage of their team's offense in respect to the team's yardage and touchdowns
* WR_BOA_twenty: the breakout age for wide receivers is defined by their age at the beginning of the college football season when they first posted a Dominator Rating at or above 20% (from playerprofiler.com)
* WR_BOA_thirty: the breakout age for wide receivers is defined by their age at the beginning of the college football season when they first posted a Dominator Rating at or above 30% (from playerprofiler.com)
* yards_per_rec_over_tm_avg: receiving yards per reception compared to the player's college team performance of receiving yards per reception
* BMI: body mass index (BMI) recorded during the NFL Combine. Formula = Mass (lb) / Height (in)^2 x 703
* Hand_Size: the distance from the tip of the pinky to the tip of the thumb with the fingers spread out (recorded at NFL combine)
* Arm_Length: the distance from the end of the bicep or shoulder blade to the tip of the middle finger with the arm extended (recorded at NFL combine)
* forty_time: time it takes a player to complete a sprint measuring 40 yards. Times not recorded at the NFL combine are adjusted by adding .05 seconds to the player time.
* Power_5_Conference: indicates whether the player played for a school belonging in one of the 'Power 5 Conferences' (Big 10, Big 12, ACC, SEC, or PAC-12) (0 = No, 1 = Yes)
* Early_Declare: indicates whether a player declared for the NFL draft before his senior year season (0 = No, 1 = Yes)
* Agility Score: a metric intended to measure a player's lateral agility and quickness
* Height Adjusted Speed Score (HaSS): an athleticism metric developed by Shawn Siegele that creates a metric for wide receivers that adjusts a player's 40 time for height.
* Relative Athletic Score (RAS): a metric created by Kent Lee Platte that can easily and intuitively gauge a player’s athletic abilities relative to the position they play
* Freak Score: an athleticism metric that accounts for the height, weight, and speed of a prospect


## File Description <a name="description"></a>
This paragraph lists the names of all notebook files, their inputs and outputs, as well as what the file does.


**`WR_clustering_public.ipynb`:**
* _Inputs_:
    * `2023_WR_Database.csv`
* _Outputs_: WR_clusters.csv
* _What it does_: This file conducts the k-means clustering analysis on the 2023_WR_Database and outputs player clusters and metrics. This file also generates a .csv file of the results to further analyze in other visualization software.


## Results
* The highest scoring players largely fall into clusters 2, 8, 14, and 10
* Cluster 2 is by far the best cluster, with 69% of the players averaging 10+ points per game over their first three seasons in the NFL 
* Cluster 2 has the best hit rate for top 5, top 12, and top 24 fantasy finishes at the wide receiver position, with ~27% of players in the cluster having at least one top 5 scoring season, 50% with a top 12 season, and 58% with a top 24 season. 
