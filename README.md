# Final Project

## My role in the group

![git_banner](gitbanner.png)

On the final project, I will fulfill the following roles: 
* Assist in choosing a dataset - completed
* Complete cleaning of dataset - completed
* Assist in further preprocessing and EDA - in process
* Create an initial plan for a database - completed
* Create a final database using PostGres - in process
* Assist with final presentation

## Initial Quick DBD for database plan
![quick_dbd](https://github.com/Megreid23/final_project/blob/main/anime%20starting%20quick%20dbd.PNG)

Data Preprocessing for database creation
1. imported csv
2. dropped columns that were not useful for analysis or didn't have enough information
3. visualized source value counts
4. binned sources into original and non-original
5. found null values and dropped rows with blank scores
6. found and dropped remaining rows with null values
7. coverted score columns floats into ints
8. visualized score value counts
9. binned scores into low, medium, and high categories
* low = 1-4
* medium = 5-6
* high = 7-9
10. convert episode floats into int
11. convert start_year into int
12. separate out genres, themes, demographics, studios, producers into their own dataframes to fix
13. genres_df
* convert list-like object columns into lists
* separate list-like column into separate columns
* determine null values in each column
* there are a little over 1000 null values which isn't exorbitant given the size of the dataset, so these can be dropped after being merged with the main anime_df
* drop all extra genre columns as they don't contribute much value to the dataset
* replace original genre values in anime_df with cleaned genres_df values
14. themes_df
* convert list-like object columns into lists
* separate list-like column into separate columns
* determine null values in each column
* there are over 4000 null values in the primary themes column and these don't add significant value to the dataset since we already have the genres
* drop themes column from anime_df
15. demographics_df
* convert list-like object columns into lists
* separate list-like column into separate columns
* determine null values in each column
* there are over 8000 null values in demographics, which means there are less than 4000 anime with demographics noted
* null values could be replaced with "None" - which is in itself interesting, as it may indicate a shift in the boys/girls mentality of anime creation - or the column may be dropped
* drop all but first column
* replace original demographic values in anime_df with cleaned anime_df values
16. studios_df
* convert list-like object columns into lists
* separate list-like column into separate columns
* determine null values in each column
* almost 2000 null values, but there may be some crossover with nulls in other new columns
* drop all but first column
* replace original studios values in anime_df with studios values in studios_df
17. producers_df
*convert list-like object columns into lists
* separate list-like column into separate columns
* determine null values in each column
* too many null values and this is a less important metric than studio
* drop producers column from anime_df
18. reinvestigate null rows
19. drop NaNs in genres column
20. drop NaNs in studios column
21. rename NaNs in demographics column as "None"
