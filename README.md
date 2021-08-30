# Clustering-Models (Unsupervised Learning)
Clustering involves automatically discovering natural grouping in data. Unlike supervised learning (like predictive modeling), clustering algorithms only interpret the input data and find natural groups or clusters in feature space. A cluster is often an area of density in the feature space where examples from the domain (observations or rows of data) are closer to the cluster than other clusters. The cluster may have a center (the centroid) that is a sample or a point feature space and may have a boundary or extent. Clustering can also be useful as a type of feature engineering, where existing and new examples can be mapped and labeled as belonging to one of the identified clusters in the data. Many algorithms use similarity or distance measures between examples in the feature space in an effort to discover dense regions of observations. As such, it is often good practice to scale data prior to using clustering algorithms. Each algorithm offers a different approach to the challenge of discovering natural groups in data. There is no best clustering algorithm, and no easy way to find the best algorithm for your data without using controlled experiments.

The different types of clustering methods can be split into:

- Connectivity-Based (Hierarchical)
- Centroid-Based
- Distribution-Based
- Density-Based
- Fuzzy (Soft)

## Connectivity-Based Clustering (Hierarchical)
Hierarchical Clustering is a distance-metric-based method of unsupervised machine learning clustering where it begins with a pre-defined top to bottom hierarchy of clusters. It then proceeds to perform a decomposition of the data objects based on this hierarchy, hence obtaining the clusters. This method follows two approaches based on the direction of progress, i.e., whether it is the top-down or bottom-up flow of creating clusters. These are Divisive Approach and the Agglomerative Approach respectively.

### Divisive Approach
This approach of hierarchical clustering follows a top-down approach where we consider that all the data points belong to one large cluster and try to divide the data into smaller groups based on a termination logic or, a point beyond which there will be no further division of data points. Hence, iteratively, we are splitting the data which was once grouped as a single large cluster, into “n” number of smaller clusters to which the data points now belong. It must be taken into account that this algorithm is highly “rigid” when splitting the clusters – meaning, when clustering is done inside a loop, there is no way that the task can be undone.

### Agglomerative Approach
Agglomerative is quite the contrary to Divisive, where all the “N” data points are considered to be a single member of “N” clusters that the data is comprised into. We iteratively combine these numerous “N” clusters to fewer number of clusters, let’s say “k” clusters and hence assign the data points to each of these clusters accordingly. This approach is a bottom-up one, and also uses a termination logic in combining the clusters.

## Centroid-Based Clustering
Centroid based clustering is considered as one of the most simplest clustering algorithms, yet the most effective way of creating clusters and assigning data points to it. The intuition behind centroid based clustering is that a cluster is characterized and represented by a central vector and data points that are in close proximity to these vectors are assigned to the respective clusters. These groups of clustering methods iteratively measure the distance between the clusters and the characteristic centroids using various distance metrics. These are either of Euclidian distance, Manhattan Distance or Minkowski Distance. The major setback here is that we should either intuitively or scientifically (Elbow Method) define the number of clusters, “k”, to begin the iteration of any clustering machine learning algorithm to start assigning the data points. Despite the flaws, Centroid based clustering has proven it’s worth over Hierarchical clustering when working with large datasets.

## Density-Based Clustering
Density-based clustering methods take density into consideration instead of distances. Clusters are considered as the most dense region in a data space, which is separated by regions of lower object density and it is defined as a maximal-set of connected points. When performing most of the clustering, we take two major assumptions, one, the data is devoid of any noise and two, the shape of the cluster so formed is purely geometrical (circular or elliptical). The fact is, data always has some extent of inconsistency (noise) which cannot be ignored. Added to that, we must not limit ourselves to a fixed attribute shape, it is desirable to have arbitrary shapes so as to not to ignore any data points. These are the areas where density based algorithms have proven their worth! Density-based algorithms can get us clusters with arbitrary shapes, clusters without any limitation in cluster sizes, clusters that contain the maximum level of homogeneity by ensuring the same levels of density within it, and also these clusters are inclusive of outliers or the noisy data.

## Distribution-Based Clustering
Distribution-based clustering creates and groups data points based on their likely hood of belonging to the same probability distribution (Gaussian, Binomial etc.) in the data. The distribution models of clustering are most closely related to statistics as it very closely relates to the way how datasets are generated and arranged using random sampling principles i.e., to fetch data points from one form of distribution. Clusters can then be easily be defined as objects that are most likely to belong to the same distribution. Distribution based clustering has a vivid advantage over the proximity and centroid based clustering methods in terms of flexibility, correctness and shape of the clusters formed. The major problem however is that these clustering methods work well only with synthetic or simulated data or with data where most of the data points most certainly belong to a predefined distribution, if not, the results will overfit.

## Fuzzy Clustering
The general idea about clustering revolves around assigning data points to mutually exclusive clusters, meaning, a data point always resides uniquely inside a cluster and it cannot belong to more than one cluster. Fuzzy clustering methods change this paradigm by assigning a data-point to multiple clusters with a quantified degree of belongingness metric. The data-points that are in proximity to the center of a cluster, may also belong in the cluster that is at a higher degree than points in the edge of a cluster. The possibility of which an element belongs to a given cluster is measured by membership coefficient that vary from 0 to 1. Fuzzy clustering can be used with datasets where the variables have a high level of overlap.

## References

Brownlee, J. (2020) 10 Clustering Algorithms With Python. Available at: https://machinelearningmastery.com/clustering-algorithms-with-python/ (Accessed: 30 August 2021)

Gupta, A. (2021) Balanced Iterative Reducing and Clustering using Hierarchies (BIRCH) Algorithm in Machine Learning. Available at: https://medium.com/geekculture/balanced-iterative-reducing-and-clustering-using-hierarchies-birch-1428bb06bb38 (Accessed: 30 August 2021)

Iliassich, L. (2016) Clustering Algorithms: From Start To State Of The Art. Available at: https://www.toptal.com/machine-learning/clustering-algorithms (Accessed: 30 August 2021)

Kassambara, A. (2019) Hierarchical Clustering in R: The Essentials. Available at: https://www.datanovia.com/en/lessons/agglomerative-hierarchical-clustering/ (Accessed: 30 August 2021)

Kaushik, S. (2016) An Introduction to Clustering and different methods of clustering. Available at: https://www.analyticsvidhya.com/blog/2016/11/an-introduction-to-clustering-and-different-methods-of-clustering/ (Accessed: 30 August 2021)

Maklin, C. (2019) Affinity Propagation Algorithm Explained. Available at: https://towardsdatascience.com/unsupervised-machine-learning-affinity-propagation-algorithm-explained-d1fef85f22c8 (Accessed: 30 August 2021)

McGregor, M. (2020) 8 Clustering Algorithms in Machine Learning that All Data Scientists Should Know. Available at: https://www.freecodecamp.org/news/8-clustering-algorithms-in-machine-learning-that-all-data-scientists-should-know/ (Accessed: 30 August 2021)

Prasad, S. (2021) Different Types of Clustering Methods and Applications. Available at: https://www.analytixlabs.co.in/blog/types-of-clustering-algorithms/ (Accessed: 30 August 2021)

Scikit-Learn (2021) Clustering. Available at: https://scikit-learn.org/stable/modules/clustering.html#affinity-propagation (Accessed: 30 August 2021)

Seif, G. (2018) The 5 Clustering Algorithms Data Scientists Need to Know. Available at: https://towardsdatascience.com/the-5-clustering-algorithms-data-scientists-need-to-know-a36d136ef68 (Accessed: 30 August 2021)

Vemula, H. (2019) How Affinity Propagation works. Available at: https://towardsdatascience.com/math-and-intuition-behind-affinity-propagation-4ec5feae5b23 (Accessed: 30 August 2021)

365 Careers (2021) The Data Science Course 2021: Complete Data Science Bootcamp. Available at: https://www.udemy.com/course/the-data-science-course-complete-data-science-bootcamp/ (Accessed: 24 August 2021)
