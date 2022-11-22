## Description of Data Cleaning & Exploration
* Drop columns that are not useful for analysis or didn't have enough information to be utilized

![drop_columns](../Images/drop_columns.PNG)

* Visualize source value counts

![sources](../Images/sources.PNG)

* Bin sources into Original and Non-original
* Drop rows with null values
* Convert score, episode, and date floats into integers
* Visualize score value counts

![scores](../Images/scores.PNG)

* Bin scores into Average and High
* Separate list-like columns of genre, themes, demographics, studios, producers, and licensors into individual columns; drop those columns with too little information to be used

![list-like_example](../Images/list-like_example.PNG)

![list-like_correction](../Images/list-like_correction.PNG)

* Re-name NaN values in demographics column as None

![final_columns](../Images/final_columns.PNG)

* Divide data into CSVs for database creation
