This lab explored clustering techniques: DBSCAN and hierarchical clustering.
**Course:** MSCS 634  
Dataset: Wine Dataset (Scikit-learn)

## Purpose of the Lab

The aim of this lab is to investigate and compare two unsupervised machine learning algorithms: Hierarchical Clustering & DBSCAN. A dataset of 178 observations with 13 numerical features (Wine) was used for this analysis to demonstrate the clustering patterns, for the evaluation of the performance of the various algorithms and for visualization of the results using PCA scatter plots and a dendrogram.

## Key Insights and Results

Three clusters were found with 58, 56 and 64 observations, using hierarchical clustering with Ward linkage. The configuration with three clusters had the highest Silhouette Score of 0.2774 for the configuration tested, which implies that the separation of the clusters is moderate.

When the parameters are set to eps=2.5 and min_samples=5, DBSCAN found 1 cluster with 24 noise points and 154 data points. The Homogeneity Score was 0.0576 and the Completeness Score was 0.1581. If noise points are removed, its Silhouette Score is undefined due to only one cluster left.

The PCA visualizations showed that Hierarchical Clustering was able to give more distinct clusters and DBSCAN was able to identify the noise observations. Overall, Hierarchical Clustering provided better separation for the selected configurations.

## Challenges and Decisions

The most challenging issue was choosing the parameter values for clustering. The number of clusters `n_clusters`, the width of the cluster defined by `eps`, and the minimum number of points in the cluster defined by `min_samples` had an important effect on the results. The features were standardized using the StandardScaler to ensure that they are in similar ranges for clustering. Two-dimensional visualization was obtained using PCA.

The choice of parameters was also crucial for DBSCAN: Small values of `eps` gave rise to numerous noise clusters while larger values resulted in fewer clusters. Several combinations of parameters were run to gain insight into these effects.

## Conclusion

Hierarchical Clustering was able to better detect clusters in the Wine dataset, while DBSCAN had the ability to detect noise. Data pre-processing, parameter tuning and clustering evaluation were pointed out by the lab.