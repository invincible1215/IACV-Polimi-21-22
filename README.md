# IACV-Polimi-21-22

## Workflow Overview

1. Download images from [Dataset](http://ubee.enseeiht.fr/dokuwiki/doku.php?id=public:toulousevpdataset#dataset)
2. Use Canny method to detect edges in images.
3. Recover straight edges within the edge maps.
4. Use the edge set obtained in step 3 as input of J-Linkage algorithm. Perform J-Linkage algorithm. The output is expected to consist of both a set of vanishing points and a classification for each edge. (Either assigned to a vanishing point or marked as an outlier.)
5. Refine the results obtained from step 5 through Expectation Maximization or other iterative algorithms.
6. Perform camera calibration given orthogonal directions of three vanishing point. 

## The output of step 2 and 3

1. A set of edges
2. The two end points of each edges
3. The centroids of the two end points
4. Implicit lines passing by edges
