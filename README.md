# CAPSTONE-PROJECT-UNSUPERVISED-NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING-

## Problem Statement
Netflix is ​​the world's largest online streaming service provider, with more than 220 million subscribers as of the second quarter of 2022. It is important for them to successfully consolidate the programs implemented on their platforms to improve user experience and thus prevent customer churn. To understand groups of programs that are similar and different from each other, we will be able to create programs that can be used to provide personalized recommendations for people to use things the way they want. The purpose of this project is to identify/group Netflix shows into specific groups so that they are shown in similar groups and shows in different groups are different from each other.
![download](https://github.com/DebnarayanMandal/NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING/assets/114856316/6f2ef889-8171-4428-9558-4857589ec2f7)

## Attribute Information
1. show_id : Unique ID for every Movie / Tv Show
2. type : Identifier - A Movie or TV Show
3. title : Title of the Movie / Tv Show
4. director : Director of the Movie
5. cast : Actors involved in the movie / show
6. country : Country where the movie / show was produced
7. date_added : Date it was added on Netflix
8. release_year : Actual Releaseyear of the movie / show
9. rating : TV Rating of the movie / show
10. duration : Total Duration - in minutes or number of seasons
11. listed_in : Genere
12. description: The Summary description

## About dataset :
Only two types of types are present in this dataset namely Movies and TV Shows. This dataset has 7787 rows and 12 columns. Only one column is in numerical format.
 
## In this project
### 1. Exploratory Data Analysis
- Top actors with higest count of movies and tv shows
- Top actors with higest count of tvshows
- Top actors with higest count of Movies
- Which words frequently use in title column
- Netflix Content Analysis
- Movies and Tv Show Duration Distribution Analysis
- How does the movie runtime vary across different genres
- Which genres have the highest number of movies produced
- Which genres have the highest number of tv show produced
- Which words frequently use in Description column
- content release over the year
- content release over the year by content type
- Highest Number of Movies and Tv Show produced by Country
- Top director with higest count of movies and tvshows
- Top rating with highest count of movies and tv show
![Annotation 2024-05-11 183538](https://github.com/DebnarayanMandal/NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING/assets/114856316/48d4d83c-f6f0-432f-b165-cf68a86f2251)

### 2. Understanding what type content is available in different countries
- Number of Movies and Tv Show produced by Country
- Number of Movies produced by Country
- Number of TV Show produced by Country
- Average Movie Duration by Country
- Country wise Rating trend
- Country wise Genres trend
![Annotation 2024-05-11 184148](https://github.com/DebnarayanMandal/NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING/assets/114856316/1647e3e7-76bb-4854-aaf5-2ba44e473aac)


### 3. Is Netflix has increasingly focusing on TV rather than movies in recent years.
![Annotation 2024-05-11 184538](https://github.com/DebnarayanMandal/NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING/assets/114856316/df8d7dd4-0e6c-4f1a-9265-543bca8d40d9)


### 4. Clustering similar content by matching text-based features
I have clustered Netflix Moves and TV Shows on the basis of Genre and Description.

For clustering, first of all punctuation marks have been removed by using 'NLTK' library in text format, then by converting the format to lower case, stop words have been removed. I used porter stemming to get the base format in words.

Through TFIDF Vectorization, I created a total of 10000 attributes.

I used Principal Component Analysis (PCA) to handle the curse of dimensionality. 3000 components were able to capture more than 88% of variance, and hence, the number of components were restricted to 3000.

To find K, the silhouette scores and elbow method are used. 16 clusters have scored the highest according to silhouette scores

Clusters are created using the K-Means clustering algorithm, and the optimal number of clusters is 16.

Final cluster visualization done using plotly library.

A content based recommender system was built using the similarity matrix obtained after using cosine similarity. This recommender system will make 10 recommendations to the user based on the type of show they watched.
![Annotation 2024-05-11 184735](https://github.com/DebnarayanMandal/NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING/assets/114856316/2624e751-4c56-41b7-b173-9e14ea406ea0)
![Annotation 2024-05-11 184824](https://github.com/DebnarayanMandal/NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING/assets/114856316/da24d86c-8cac-4b26-a765-d7397dad28c5)

![Annotation 2024-05-11 184847](https://github.com/DebnarayanMandal/NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING/assets/114856316/c4b2fc13-6e09-4aa3-8cef-51db4788d23c)














