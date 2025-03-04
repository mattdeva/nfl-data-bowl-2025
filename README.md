# Overview

The Kaggle NFL Data Bowl is a yearly data science competition in which participants use Next Gen Stats player tracking data to generate a significant statistic. The prompt for 2025 was to use pre-snap behavior to predict and better understand NFL team and player tendencies. My submission for the competition includes generating an actionable prediction/metric and completing an analysis to justify its usefulness. See kaggle competiiton page for full details: [Kaggle NFL Data Bowl 25](https://www.kaggle.com/code/mattneel/block-dislocation-index-nfl-data-bowl-25)

# Submission

The premise behind the metric I developed is simple; the offense should direct its runs towards defenders that are easiest to move. My metric, Block Dislocation Index, captures how movable a defender is during a run play relative to all other defenders. The implementation of the metric is a simple as the premise. Prior to the snap, the offense could asses where the most movable players were, and aim the runs into that direciton. In the full analysis, I walk through the development of the metric as well as insights from potential implemmentation [Submission Notebook](https://www.kaggle.com/code/mattneel/block-dislocation-index-nfl-data-bowl-25)

# Data Curation

To develop my metric, Kaggle provided data tables for games, players, plays, and player tracking. For the metric to be a viable, it needed to include player the tracking table.

I was able to use the player tracking data to create a table of blocks on running plays. This table included defenders who were engaged with a opposing player or two opposing players, which facing in opposite directions. From this table, I was able to determine the starting and stopping point of the block and calucate the amount of yards ceded (or gained) by the defender during the block. I refered to yards ceded as Block Dislocation in the official sumbission and in the final metric. A full description of how the Index was created can be found in the submission above.

A notebook of the data processing into the blocks table is saved to the repo [Dataprep Notebook](https://github.com/mattdeva/nfl-data-bowl-2025/blob/main/dataprep-final.ipynb)
