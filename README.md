# sql-assignment
in trying to import a csv file i had trouble trying to get the tables to show in the schema section
tables were automatically created from the list of neflix shows i created

 What are the most popular TV shows or movies in terms of the number of titles?
To answer this, we can use a simple COUNT query to find the total number of titles in the dataset.
SQL Query:
SQL

SELECT COUNT(*) AS Total_Titles
FROM media_catalog;
 Which TV shows or movies have the highest ratings (if available)?
Assuming there’s a column for ratings (e.g., “rating” or “imdb_rating”), we can use an ORDER BY query to sort the titles by rating in descending order.
SQL Query:
SQL

SELECT title, rating
FROM media_catalog
WHERE rating IS NOT NULL
ORDER BY rating DESC
LIMIT 10;
