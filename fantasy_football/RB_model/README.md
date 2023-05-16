# Clustering NFL Running Backs to Improve Fantasy Football Rookie Draft Outcomes

## Table of Contents
* [Installation](#Installation)
* [Project Motivation and Description](#motivation)
* [File Description](#description)
* [Results](#Results)


## Installation
The code requires Python versions of 3.* as well as the following:
* pandas
* numpy
* matplotlib.pyplot
* seaborn as sns
* math


## Project Objective and Description <a name="motivation"></a>
The objective of this project is to use k-means unsupervised learning to cluster similar NFL running backs together in an attempt to improve fantasy football rookie draft decisions. The model is built using data involving players' NCAA stats and NFL combine data. The features and their descriptions are below:

Feature Description:
* DP: draft pick where player was selected in the NFL draft
* Rush_ATT_per_GP: rushing attempts per game
* Rush_Yards_per_GP: rushing yards per game
* Rush_TDs_per_GP: rushing touchdownds per game
* Yards_per_Carry: rushing yards per carry (rushing attempt)
* REC_per_GP: receptions per game
* REC_Yards_per_GP: receiving yards per game
* REC_TDs_per_GP: receiving touchdowns per game
* Yards_per_REC: yards gained per receptions
* Touches_per_GP: touches per game
* PPR_per_GP: average fantasy points per game (PPR style scoring) in college
* Combined_RUSH_MS: a metric designed to represent a player's production in their team's rushing offense.
* Combined_REC_MS: a metric designed to represent a player's receiving production in their college offense
* RUSH_CD: a metric that equally weighs the career last and career best seasons in terms of market share of team rushing yards and rushing touchdowns.
* REC_CD: represents the player's percentage of their team's offense in respect to the team's yardage and touchdowns
* RB_BOA: the age in a season a running back first achieves a greater than 15% scrimmage dominator rating.
* Yards_per_Carry_Over_TM_AVG: rushing yards per carry compared to the player's college team performance of rushing yards per carry
* Yards_per_TM_Rush_ATT: player's rushing yards divided by player's team rush attempts in a season
* BMI: body mass index (BMI) recorded during the NFL Combine. Formula = Mass (lb) / Height (in)^2 x 703
* forty_time: time it takes a player to complete a sprint measuring 40 yards. Times not recorded at the NFL combine are adjusted by adding .05 seconds to the player time.
* Agility_Score: a metric intended to measure a player's lateral agility and quickness
* Broad: measures the player's ability to jump horizontally from a balanced stance
* Weight Adjusted Speed Score (WaSS): an athleticism metric developed by Bill Barnwell in Pro Football Prospectus that adjusts a player's 40 yard dash time for their weight
* Relative Athletic Score (RAS): a metric created by Kent Lee Platte that can easily and intuitively gauge a player’s athletic abilities relative to the position they play
* Power_5_Conference: indicates whether the player played for a school belonging in one of the 'Power 5 Conferences' (Big 10, Big 12, ACC, SEC, or PAC-12) (0 = No, 1 = Yes)
* Early_Declare: indicates whether a player declared for the NFL draft before his senior year season (0 = No, 1 = Yes)


## File Description <a name="description"></a>
This paragraph lists the names of all notebook files, their inputs and outputs, as well as what the file does.


**`RB_clustering_public.ipynb`:**
* _Inputs_:
    * `2023_RB_Database.csv`
* _Outputs_: RB_clusters.csv
* _What it does_: This file conducts the k-means clustering analysis on the 2023_RB_Database and outputs player clusters and metrics. This file also generates a .csv file of the results to further analyze in other visualization software.


## Results
* The highest scoring players largely fall into clusters 0, 4, 6, and 10
* Cluster 0 is by far the best cluster, with 76% of the players averaging 10+ points per game over their first three seasons in the NFL - players in this cluster should be highly considered while drafting
* Cluster 0 has the highest hit rate for top 5, top 12, and top 24 fantasy finishes at the running back position, with 48% of players in the cluster having at least one top 5 scoring season, 64% with a top 12 season, and 76% with a top 24 season
