# Clustering-Analysis-on-Movies-TV-shows-Unsupervised-ML
![image](https://user-images.githubusercontent.com/95495685/185733165-1cbdbb8a-22f3-4dde-acd3-dc729af13099.png)



Introduction
Netflix’s recommendation system gives the idea to them about the popularity of their services provides as it help to increase the sold the subscriptions as more as possible,which offers a varieties of items for selections, this help to get them a user satisfaction,and their loyalty to platform and get them a better understanding of what the user wants.

Then it’s easier to get the user to make better decisions from a wide variety of movie products.

With over 139 million paid subscribers(total viewer pool -300 million) across 190 countries, 15,400 titles across its regional libraries and 112 Emmy Award Nominations in 2018 — Netflix is the leading Internet television network and the most-valued largest streaming service in the world. The success behind the amazing story of Netflix is incomplete without the mention of its recommender systems that focus on personalization according to users. According to your preferences,there are several methods to create a list of recommendations.You can use (Collaborative-filtering) and (Content-based Filtering) for recommendation.

Problem Statement
This dataset consists of tv shows and movies available on Netflix as of 2019. The dataset is collected from Flexible which is a third-party Netflix search engine. In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service’s number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. It will be interesting to explore what all other insights can be obtained from the same dataset.

In this project, we are evaluating as below-

Exploratory Data Analysis
Understanding what type content is available in different countries
Is Netflix increasingly focused on TV rather than movies in recent years?
Clustering similar content by matching text-based features
Objective
The project's main goal is to create a model that can perform Clustering on comparable material by matching text-based attributes.

Dataset Peeping
The dataset has 7787 rows and 12 attributes to work with.

We have NaN values in the dataset.
Changed the format of the Date.
Added some columns which are extracted from the Date column.
Approach
As per the problem statement, understanding what type of content is available in different countries and Is Netflix increasingly focused on TV rather than movies in recent years we have to do clustering on similar content by matching text-based features. For that we used Agglomerative Clustering, and K-means Clustering.

Feature Engineering
● There are too much classes, so we just obtain the first 50 (the most common 50) ● Unify some of the similar types(genre) ● Make a dictionary with similar content by matching text-based features that we are going to use in clustering.

Correlation Heatmap
image

Hypothesis Evaluation
imageimage

Hypothesis from the data visualized-

According to the first graph, the number of TV shows launched in the previous few years is growing.
According to the second graph, the number of TV shows added to Netflix is stable.
Building a clustering model
Clustering models allow you to categorize records into a certain number of clusters. This can help you identify natural groups in your data.

Clustering models focus on identifying groups of similar records and labeling the records according to the group to which they belong. This is done without the benefit of prior knowledge about the groups and their characteristics. In fact, you may not even know exactly how many groups to look for. This is what distinguishes clustering models from the other machine-learning techniques—there is no predefined output or target field for the model to predict. These models are often referred to as unsupervised learning models, since there is no external standard by which to judge the model's classification performance.

Model Implementation
1. Agglomerative Clustering-
The agglomerative clustering is the most common type of hierarchical clustering used to group objects in clusters based on their similarity.Next, pairs of clusters are successively merged until all clusters have been merged into one big cluster containing all objects. We used a dendrogram to find the number of clusters. image

2. K-means Clustering
k-means clustering is a method of vector quantization, originally from signal processing, that aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean (cluster centers or cluster centroid), serving as a prototype of the cluster. We created the sample data using build blobs and used range_n_clusters to specify the number of clusters we wanted to utilize in k means.

Metrics: Silhouette Coefficient or silhouette score-
Silhouette analysis can be used to study the separation distance between the resulting clusters. The silhouette plot displays a measure of how close each point in one cluster is to points in the neighboring clusters and thus provides a way to assess parameters like number of clusters visually. This measure has a range of [-1, 1]. Silhouette coefficients (as these values are referred to as) near +1 indicate that the sample is far away from the neighboring clusters. A value of 0 indicates that the sample is on or very close to the decision boundary between two neighboring clusters and negative values indicate that those samples might have been assigned to the wrong cluster.

Conclusion-
Most films were released in the years 2018, 2019, and 2020.
TV shows account for 2.8 percent of the total, while movies account for 97.2 percent.
Dramas is a genre that is mostly watched on Netflix and as per audience preference international movies are mostly watched.
The largest count of Netflix content is made with a “TV-14” rating,
The United States, India, the United Kingdom, Canada, and Egypt are the top five producer countries.
Netflix has added a lot more movies and TV episodes in the previous years, but the numbers are still low when compared to movies released in the last ten years.
Movies are mostly watched in various countries rather than TV shows.
We performed data engineering to remove the unnecessary variables and to convert the data into standardized form into scalar.
We used the Agglomerative Clustering model with dendrogram to obtain the clusters= 4 which gave the silhouette score as 0.19676189959151683.This score is not good so to improve the model we utilized the K-means clustering model.
Implemented model is based on the K-means clustering algorithm consisting of 2,3,4,5,6 clusters. Silhouette Analysis score for K-means : ● For n_clusters = 2 The average silhouette_score is : 0.7049787496083262 ● For n_clusters = 3 The average silhouette_score is : 0.5882004012129721 ● For n_clusters = 4 The average silhouette_score is : 0.6505186632729437 ● For n_clusters = 5 The average silhouette_score is : 0.56376469026194 ● For n_clusters = 6 The average silhouette_score is : 0.4504666294372765
After clustering, we can say that our alternative hypothesis is that the number of TV shows launched in the previous few years is NOT growing.
Our second alternative hypothesis is the number of TV shows added to Netflix is higher.
Thank You
