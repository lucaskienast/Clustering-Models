# Clustering Models (Unsupervised Learning)
Overview of theory and common techniques for clustering problems, split into:

- Connectivity-Based (Hierarchical)
- Centroid-Based
- Distribution-Based
- Density-Based
- Constraint-Based (Semi-Supervised)
- Fuzzy (Soft)
- Cluster Performance

## Installation
Use `git clone` to get a copy of this repository.
```
$ git clone https://github.com/lucaskienast/Clustering-Models.git
$ cd Clustering-Models
```
## Connectivity-Based Clustering (Hierarchical)
Hierarchical Clustering is a distance-metric-based method of unsupervised machine learning clustering where it begins with a pre-defined top to bottom hierarchy of clusters. It then proceeds to perform a decomposition of the data objects based on this hierarchy, hence obtaining the clusters. This method follows two approaches based on the direction of progress, i.e., whether it is the top-down or bottom-up flow of creating clusters. These are Divisive Approach and the Agglomerative Approach respectively.

Usage:

You can use hierarchical clustering if your data is hierarchical. It is also good to use when your dataset is randomized. You can use hierarchical clustering to classify elements — such as animals, products, research topic, etc. Unlike partition-based algorithms, a hierarchy-based algorithm doesn’t need a fixed number of clusters. The algorithms will produce a visual representation of the resultant clusters for better interpretation and understanding.

Pros:

- Easy to implement
- Number of clusters need not be specified a priori
- Dendrograms are easy to interpret

Cons:

- Cluster assignment is strict and cannot be undone
- High time complexity
- Cannot work for a larger dataset

## Centroid-Based Clustering (Partitioning)
Centroid based clustering is considered as one of the most simplest clustering algorithms, yet the most effective way of creating clusters and assigning data points to it. The intuition behind centroid based clustering is that a cluster is characterized and represented by a central vector and data points that are in close proximity to these vectors are assigned to the respective clusters. These groups of clustering methods iteratively measure the distance between the clusters and the characteristic centroids using various distance metrics. These are either of Euclidian distance, Manhattan Distance or Minkowski Distance. The major setback here is that we should either intuitively or scientifically (Elbow Method) define the number of clusters, “k”, to begin the iteration of any clustering machine learning algorithm to start assigning the data points. Despite the flaws, Centroid based clustering has proven it’s worth over Hierarchical clustering when working with large datasets.

Usage:

The partition-based clustering algorithms are best used with categorical data — for example, grouping the data based on gender, age group, or education level. Moreover, most partition-based algorithms are simple, fast, and highly scalable. The down-side to these algorithms is that their performance depends on the initial number of centroids and the outliers in a dataset.

Pros:

- Easy to implement
- Fast processing
- Can work on larger data
- Easy to interpret the outputs

Cons:

- Need to specify number of centroids a priori
- Clusters that get created are of inconsistent sizes and densities
- Affected by noise and outliers

## Density-Based Clustering
In density-based clustering, algorithms form the different clusters based on the data region's density at any given location. Using this approach, arbitrary-shaped distributions are formed in dense areas of the data. These types of algorithms struggle with data of varying densities or data with high dimensionality. The two well-known algorithms of this type are DBSCAN and OPTICS. Such algorithms are used in applications such as contact tracing for infectious diseases.

Usage:

These algorithms can analyze data and make predictions and hence can be used in various applications, such as contact tracing, marketing strategies development. Density-based clustering is also a good choice if your data contains noise or your resulted cluster can be of arbitrary shapes. Moreover, these types of algorithms can deal with dataset outliers more efficiently than the other types of algorithms.

Pros:

- Can handle noise and outliers
- Need not specify number of clusters a priori
- Created clusters are highly homogeneous
- No restrictions on cluster shapes

Cons:

- Complex and slow algorithm
- Cannot be scaled to larger datasets

## Distribution-Based Clustering
Distribution-based clustering creates and groups data points based on their likely hood of belonging to the same probability distribution (Gaussian, Binomial etc.) in the data. The distribution models of clustering are most closely related to statistics as it very closely relates to the way how datasets are generated and arranged using random sampling principles i.e., to fetch data points from one form of distribution. Clusters can then be easily be defined as objects that are most likely to belong to the same distribution. Distribution based clustering has a vivid advantage over the proximity and centroid based clustering methods in terms of flexibility, correctness and shape of the clusters formed. The major problem however is that these clustering methods work well only with synthetic or simulated data or with data where most of the data points most certainly belong to a predefined distribution, if not, the results will overfit.

Usage:

Distribution-based clustering can be used to mine large datasets and produces complex models for clusters. Doing so reveals the correlation and dependence between the different data points.

Pros:

- Need not specify number of clusters a priori
- Works on real time data
- Metrics are easy to understand and tune

Cons:

- Complex and slow algorithm
- Cannot be scaled to larger datasets

## Constraint-Based Clustering (Semi-Supervised)
In computer science, constrained clustering is a class of semi-supervised learning algorithms. Typically, constrained clustering incorporates either a set of must-link constraints, cannot-link constraints, or both, with a Data clustering algorithm. Both a must-link and a cannot-link constraint define a relationship between two data instances. A must-link constraint is used to specify that the two instances in the must-link relation should be associated with the same cluster. A cannot-link constraint is used to specify that the two instances in the cannot-link relation should not be associated with the same cluster. These sets of constraints acts as a guide for which a constrained clustering algorithm will attempt to find clusters in a data set which satisfy the specified must-link and cannot-link constraints. Some constrained clustering algorithms will abort if no such clustering exists which satisfies the specified constraints. Others will try to minimize the amount of constraint violation should it be impossible to find a clustering which satisfies the constraints. Constraints could also be used to guide the selection of a clustering model among several possible solutions.

Usage:

Constraint-based clustering is used when you have unlabeled data that needs to be clustered into groups of known characteristics or criteria. Define these criteria and feed them into the model.

Pros:

- Creates a perfect decision boundary
- Can automatically determine the outcome classes based on cluster constraints
- Future data can be clustered and classified based on training boundaries

Cons:

- Overfitting likely
- High level of misclassification errors
- Cannot be trained on larger datasets

## Fuzzy Clustering
The general idea about clustering revolves around assigning data points to mutually exclusive clusters, meaning, a data point always resides uniquely inside a cluster and it cannot belong to more than one cluster. Fuzzy clustering methods change this paradigm by assigning a data-point to multiple clusters with a quantified degree of belongingness metric. The data-points that are in proximity to the center of a cluster, may also belong in the cluster that is at a higher degree than points in the edge of a cluster. The possibility of which an element belongs to a given cluster is measured by membership coefficient that vary from 0 to 1. Fuzzy clustering can be used with datasets where the variables have a high level of overlap.

Usage: 

Fuzzy theory-based algorithms are well suited for application that requires multiple clusters for the same data point. For example, it can be used in marketing to cluster the preferences and shopping patterns of clients more realistically and help create a more personalized shopping experience.

Pros:

- Can work on highly overlapped data
- A higher rate of convergence

Cons:

- Need to specify number of centroids a priori
- Affected by noise and outliers
- Slow algorithm
- Cannot be scaled

## Cluster Performance
Evaluating the performance of a clustering algorithm is not as trivial as counting the number of errors or the precision and recall of a supervised classification algorithm. In particular any evaluation metric should not take the absolute values of the cluster labels into account but rather if this clustering define separations of the data similar to some ground truth set of classes or satisfying some assumption such that members belong to the same class are more similar than members of different classes according to some similarity metric. Methods include:

Ground truth known:

- Rand index
- Mutual information based scores
- Homogeneity, completeness and V-measure
- Fowlkes-Mallows scores 
- Contingency matrix 
- Pair confusion matrix 

Ground truth unkown:

- Silhouette coefficient
- Calinski-Harabasz index / Variance Ratio Criterion 
- Davies-Bouldin index 

## References

Brownlee, J. (2020) 10 Clustering Algorithms With Python. Available at: https://machinelearningmastery.com/clustering-algorithms-with-python/ (Accessed: 30 August 2021)

Doshi, N. (2019) Spectral Clustering. Available at: https://towardsdatascience.com/spectral-clustering-82d3cff3d3b7 (Accessed: 30 August 2021)

Fleshman, W. (2019) Spectral Clustering. Available at: https://towardsdatascience.com/spectral-clustering-aba2640c0d5b#:~:text=Spectral%20clustering%20is%20a%20technique,non%20graph%20data%20as%20well. (Accessed: 30 August 2021)

Garbade, M. (2018) Understanding K-Means Clustering in Machine Learning. Available at: https://towardsdatascience.com/understanding-k-means-clustering-in-machine-learning-6a6e67336aa1 (Accessed: 30 August 2021)

Gupta, A. (2021) Balanced Iterative Reducing and Clustering using Hierarchies (BIRCH) Algorithm in Machine Learning. Available at: https://medium.com/geekculture/balanced-iterative-reducing-and-clustering-using-hierarchies-birch-1428bb06bb38 (Accessed: 30 August 2021)

Iliassich, L. (2016) Clustering Algorithms: From Start To State Of The Art. Available at: https://www.toptal.com/machine-learning/clustering-algorithms (Accessed: 30 August 2021)

Kassambara, A. (2019) Hierarchical Clustering in R: The Essentials. Available at: https://www.datanovia.com/en/lessons/agglomerative-hierarchical-clustering/ (Accessed: 30 August 2021)

Kaushik, S. (2016) An Introduction to Clustering and different methods of clustering. Available at: https://www.analyticsvidhya.com/blog/2016/11/an-introduction-to-clustering-and-different-methods-of-clustering/ (Accessed: 30 August 2021)

Keerthz (2021) What, why and how of Spectral Clustering. Available at: https://www.analyticsvidhya.com/blog/2021/05/what-why-and-how-of-spectral-clustering/ (Accessed: 30 August 2021)

Maklin, C. (2019) Affinity Propagation Algorithm Explained. Available at: https://towardsdatascience.com/unsupervised-machine-learning-affinity-propagation-algorithm-explained-d1fef85f22c8 (Accessed: 30 August 2021)

McGregor, M. (2020) 8 Clustering Algorithms in Machine Learning that All Data Scientists Should Know. Available at: https://www.freecodecamp.org/news/8-clustering-algorithms-in-machine-learning-that-all-data-scientists-should-know/ (Accessed: 30 August 2021)

Metwalli, S. (2020) Clustering 101: How to Choose the Right Algorithm for Your Application. Available at: https://towardsdatascience.com/clustering-101-how-to-choose-the-right-algorithm-for-your-application-fb1521ea13fc (Accessed: 30 August 2021)

Prasad, S. (2021) Different Types of Clustering Methods and Applications. Available at: https://www.analytixlabs.co.in/blog/types-of-clustering-algorithms/ (Accessed: 30 August 2021)

Rajan, S. (2020) Overview of Clustering Algorithms. Available at: https://towardsdatascience.com/overview-of-clustering-algorithms-27e979e3724d (Accessed: 30 August 2021)

Scikit-Learn (2021) Clustering. Available at: https://scikit-learn.org/stable/modules/clustering.html#affinity-propagation (Accessed: 30 August 2021)

Seif, G. (2018) The 5 Clustering Algorithms Data Scientists Need to Know. Available at: https://towardsdatascience.com/the-5-clustering-algorithms-data-scientists-need-to-know-a36d136ef68 (Accessed: 30 August 2021)

Sinclair, C. (2019) Clustering Using OPTICS. Available at: https://towardsdatascience.com/clustering-using-optics-cac1d10ed7a7 (Accessed: 30 August 2021)

Singh, A. (2019) Build Better and Accurate Clusters with Gaussian Mixture Models. Available at: https://www.analyticsvidhya.com/blog/2019/10/gaussian-mixture-models-clustering/ (Accessed: 30 August 2021)

Thompson, J. (2019) Choosing the Right Clustering Algorithm for your Dataset. Available at: https://www.kdnuggets.com/2019/10/right-clustering-algorithm.html (Accessed: 30 August 2021)

Vemula, H. (2019) How Affinity Propagation works. Available at: https://towardsdatascience.com/math-and-intuition-behind-affinity-propagation-4ec5feae5b23 (Accessed: 30 August 2021)

Wikipedia (2021) Constrained Clustering. Available at: https://en.wikipedia.org/wiki/Constrained_clustering (Accessed: 30 August 2021)

Yildirim, S. (2020) DBSCAN Clustering - Explained. Available at: https://towardsdatascience.com/dbscan-clustering-explained-97556a2ad556 (Accessed: 30 August 2021)

365 Careers (2021) The Data Science Course 2021: Complete Data Science Bootcamp. Available at: https://www.udemy.com/course/the-data-science-course-complete-data-science-bootcamp/ (Accessed: 24 August 2021)
