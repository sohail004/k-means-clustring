# k-means-clustring
Clustering means grouping things which are similar or have features in common and so is the purpose of k−means clustering. K−means clustering is an unsupervised machine learning algorithm for clustering ’n’ observations into ‘k’ clusters where k is predefined or user− defined constant. The main idea is to define k centroids, one for each cluster.

The K Means algorithm involves:
Choosing the number of clusters “k”.
Randomly assign each point to a cluster.
Until clusters stop changing, repeat the following:
For each cluster, compute the cluster centroid by taking the mean vector of points in the cluster.
Assign each data point to the cluster for which the centroid is the closest.
Two things are very important in K means, the first is to scale the variables before clustering the data, and second is to look at a scatter plot or a data table to estimate the number of cluster centres to set for the k parameter in the model.
Choosing the optimal K value:
One way of choosing the k value is to use the elbow method. First, you compute the sum of squared error (SSE) for some values of k. SSE is the sum of the squared distance between each member of the cluster and its centroid. If you plot k against the SSE, you will see that the error decreases with increasing k. This is because as the number of clusters increases,
the error should be smaller and therefore, distortion should be smaller. The idea of the elbow method is to choose the k value at which the SSE decreases significantly.
Applications of K-Means Clustering:

k−means can be applied to data that has a smaller number of dimensions, is numeric, and is continuous. such as document clustering, identifying crime−prone areas, customer segmentation, insurance fraud detection, public transport data analysis, clustering of IT alerts…etc.


Challenges with the K-Means Clustering Algorithm
One of the common challenges we face while working with K-Means is that the size of clusters is different. Let’s say we have the below points:
 
 




The left and the rightmost clusters are of smaller size compared to the central cluster. Now, if we apply k-means clustering on these points, the results will be something like this:




Another challenge with k-means is when the densities of the original points are different. Let’s say these are the original points:
 
 




Here, the points in the red cluster are spread out whereas the points in the remaining clusters are closely packed together. Now, if we apply k-means on these points, we will get clusters like this:







We can see that the compact points have been assigned to a single cluster. Whereas the points that are spread loosely but were in the same cluster, have been assigned to different clusters. Not ideal so what can we do about this?
 
One of the solutions is to use a higher number of clusters. So, in all the above scenarios, instead of using 3 clusters, we can have a bigger number. Perhaps setting k=10 might lead to more meaningful clusters.

Remember how we randomly initialize the centroids in k-means clustering? Well, this is also potentially problematic because we might get different clusters every time. So, to solve this problem of random initialization, there is an algorithm called K-
Means++ that can be used to choose the initial values, or the initial cluster centroids, for K-Means.
