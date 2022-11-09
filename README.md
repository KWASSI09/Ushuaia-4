# Music Oracle
![](image/467733455_orig.jpg)

## 📝 Project Overview
Besides being a medium for entertainment, music is an incredible and powerful language that allows us to express our emotions and feelings. In some cases, music can prove to be efficient on a therapeutic level, especially in particular moments of our life. As emotions and moods can easily be reflected in music, we all try to use it in every moment of our daily life based on our current state of mind, whether we are looking for a stimulant or comfort to calm us down, to sleep, or for sport. The combination of all these aspects is, in fact, the reason why we decided to find a classification model able to help us determine the type of mood of a song. 

## ETL process
### In the transfromation.ipynb file
1. After downloading our two files from Kaggle, we imported them into jupyter notebook and created data frames using pandas.
Subsequently, we performed a cleaning procedure involving identifying data errors and removing columns not used in our analysis; we also eliminated any empty cells. This phase aims to improve the quality of the data and to have more accurate, consistent and reliable information for the continuation of the project.
![](/image/transformation.png)

2. After transforming the data, using SQL Alchemy, we built a connection between Jupyter notebook and PostgreSQL, where we had previously created a database and two tables to hold our data.
The choice of Postgres was because our two tables have a comune column for which a relational database was ideal.
![](image/dbconn.png)

## Data analysis
### In the Analysis.ipynb file

1. In this part of our project, we selected nine features from our dataset to conduct our analysis on Spotify music and displayed a statistic summary to summarise and provide a gist of information about our dataset. 
We then displayed the correlations between each selected feature which led us to plot our data's heatmap.
![](image/heatmap.png)

      * In the heatmap, the positive value means that the two attributes have positive correlation between them
      * The colors are darker or lighter based on the correletion value inside our interval (-1,1). 
2. We then used Seaborn Pairplot that allows us to plot pairwise relationships between our selected features with the track mood. This creates a nice visualisation and helps us understand the data by summarising a large amount of data in a single figure. This is essential when we are exploring our dataset and trying to become familiar with it. In the figure, we can see all our variables shown along the y and x axis. Along the diagonal we have a kernel density estimate(KDE) showing the clustering of each of the variables considering the mood.  
![](image/pairplot.png)

3. We also displayed an histogram of each selected features showing the distrubition of the selected features
# Tableau visualization
With tableau, se created few visualizations highlighting certain charateristics of our dataset. We managed to vizualise patterns such as:
* The top 10 popular artists
* The top popular songs
* Acousticness track count and percentage per mood
* Danceability track count and percentage per mood
* Amount of tracks per decade of release considering the mood
* Top 10 popular track per mood

Click the link to see the tableau workbook 
https://public.tableau.com/app/profile/kouam.kouassi/viz/My_song_oracle/top10populartrackpermood


## Prediction Process and codes
### In the Prediction.ipynb file
This file contains our machine learning and neural network models applied in the song mood prediction.


## 📚 Dataset Sources:


* https://www.kaggle.com/datasets/musicblogger/spotify-music-data-to-identify-the-moods


