# Clustering NFL Running Backs to Improve Fantasy Football Rookie Draft Outcomes

This project is part of my Master thesis investigating whether prior CSR-related professional experience of directors sitting on boards of companies affects the corporate social performance (CSP) of those companies. CSR stands for corporate social responsibility and describes company conduct that is guided not only by economic concerns, but also by concerns about the environment, society, stakeholders and other discretionary factors. I investigated two hypothesis and both were supported.


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


## Project Motivation and Description <a name="motivation"></a>


## File Description <a name="description"></a>
This paragraph lists the names of all jupyter notebook files, their inputs and their outputs, as well as what the file does.

**`RB_clustering_public.ipynb`:**
* _Inputs_:
    * `2023_RB_Database.csv`
* _Outputs_: RB_clusters.csv
* _What it does_: This file conducts the k-means clustering analysis on the 2023_RB_Database and outputs 
* 
* NFL running backs  their corresponding clusters


## Results
Observing the cluster dataframe, the highest scoring players fall into clusters 0, 4, 6, and 10. Cluster 0 is by far the best cluster, with 76% of the players averaging 10+ points per game over their first three seasons in the NFL. This cluster also has the highest hit rate for top 5, top 12, and top 24 fantasy finishes at the running back position, with 48% of players in the cluster having at least one top 5 scoring season, 64% with a top 12 season, and 76% with a top 24 season. With high scoring running backs greatly contributing to overall fantasy team success, players in this cluster should be heavily considered when drafting players. After cluster 11 there is a steep dropoff in fantasy scoring. These players would be better targets for very late rounds as the clusters are much less likley to provide fantasy value.
