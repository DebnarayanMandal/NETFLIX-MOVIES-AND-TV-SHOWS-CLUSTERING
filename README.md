# CAPSTONE-PROJECT-UNSUPERVISED-NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING-

## Problem Statement
Netflix is ​​the world's largest online streaming service provider, with more than 220 million subscribers as of the second quarter of 2022. It is important for them to successfully consolidate the programs implemented on their platforms to improve user experience and thus prevent customer churn. To understand groups of programs that are similar and different from each other, we will be able to create programs that can be used to provide personalized recommendations for people to use things the way they want. The purpose of this project is to identify/group Netflix shows into specific groups so that they are shown in similar groups and shows in different groups are different from each other.

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

### 2. Understanding what type content is available in different countries
- Number of Movies and Tv Show produced by Country
- Number of Movies produced by Country
- Number of TV Show produced by Country
- Average Movie Duration by Country
- Country wise Rating trend
- Country wise Genres trend


### 3. Is Netflix has increasingly focusing on TV rather than movies in recent years.


### 4. Clustering similar content by matching text-based features
I have clustered Netflix Moves and TV Shows on the basis of Genre and Description.

For clustering, first of all punctuation marks have been removed by using 'NLTK' library in text format, then by converting the format to lower case, stop words have been removed. I used porter stemming to get the base format in words.

Through TFIDF Vectorization, I created a total of 10000 attributes.

I used Principal Component Analysis (PCA) to handle the curse of dimensionality. 3000 components were able to capture more than 88% of variance, and hence, the number of components were restricted to 3000.

To find K, the silhouette scores and elbow method are used. 16 clusters have scored the highest according to silhouette scores

Clusters are created using the K-Means clustering algorithm, and the optimal number of clusters is 16.

Final cluster visualization done using plotly library.

A content based recommender system was built using the similarity matrix obtained after using cosine similarity. This recommender system will make 10 recommendations to the user based on the type of show they watched.




## Objective
The objective of using PCA (Principal Component Analysis) in a face recognition system is to reduce the dimensionality of the face images while preserving the most important information necessary for accurate recognition. Here's how PCA is typically applied in a face recognition system:

Dimensionality Reduction: Face images are typically high-dimensional, especially if they are in color or high-resolution. PCA is used to reduce the dimensionality of these images by finding a set of orthogonal axes (principal components) that capture the maximum variance in the data.

Feature Extraction: Each face image is treated as a point in a high-dimensional space. PCA transforms these points into a lower-dimensional space, where each image is represented by a vector of reduced dimensionality. These vectors are the principal components that capture the essential features of the face images.

Eigenfaces: The principal components obtained from PCA are often referred to as eigenfaces. These eigenfaces represent the directions of maximum variance in the face image dataset. They can be thought of as "generic face patterns" that capture the main variations in facial appearance across the dataset.

Recognition: During the recognition phase, a new face image is projected onto the lower-dimensional subspace spanned by the eigenfaces. This projection results in a low-dimensional representation of the new face image. By comparing this representation with those of known faces (stored in a database), the system can identify or verify the identity of the person in the new image.

Classification: The reduced-dimensional representations of face images can be used as input to classification algorithms (such as k-nearest neighbors or support vector machines) and characteristics.

Overall, the objective of using PCA in a face recognition system is to improve computational efficiency, reduce storage requirements, and enhance recognition accuracy by extracting and representing the essential features of face images in a lower-dimensional space.







## FACE COLLECTION

Before, we test the face recognition technique we need to collection of human
face images. That’s why we need to collect human face images in vary angle and
also lighting, darkness, inside home and outside home images as well. We take
a ORL dataset that have same kind of images, next I using PCA and 2D PCA on
ORL dataset to find out how to accurately work in face recognition technique.
## Result
There I discuss what kind of result and accuracy I get.
## CONCLUSION
In this research, I attempt to investigate one types of Principal Component
Technique and 1D Principal Component Technique methodologies. I also spoke
about what other people believe about PCA . I just only use ORL
dataset for find out the facial recognition. Inside my dataset have all pixel value,
then I converted all pixel values to image format than use PCA for
facial recognition with using of Eigen-faces. And training images were cropped
from each subject's original face to a smaller area ear to ear horizontally and
forehead to lips vertically. Meanwhile, the same different classification was not
found when a non-library input image was evaluated.
There, I showed a number of algorithms for face identification under uncontrolled
illumination depending on the center region of the face being considered normal,
bright, very bright, or dark. Finally, this method shows a promising and good
results but it’s still needs to be explored.