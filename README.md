Predicting Air Production Unit (APU) failures in metro train operations is a critical challenge with profound implications for maintenance efficiency and operational reliability. Traditionally, preventive and reactive maintenance strategies have been employed, often relying on predefined schedules or post-failure responses. The MetroPT-3 dataset is a valuable repository encapsulating the heartbeat of metro train operations. Derived from real-world readings within a compressor’s Air Production Unit (APU), this dataset provides a comprehensive insight into the operational dynamics of metro systems (https://archive.ics.uci.edu/dataset/791/metropt+3+dataset). Collected parameters, including pressure, temperature, motor current, and air intake valves, offer a granular perspective on the intricate interplay of factors influencing APU functionality.

This project aims to identify instances of APU failures thus requiring maintenance. To effectively predict failures and spot issues in metro train systems, multiple data mining techniques in addition to machine learning classifiers were used to be able to detect instances with APU failures. Data mining approaches were applied to 4 different variants of the dataset, each constituting an approach, which are:
1. Applications on the full dataset
2. Applications on 2 principle components on the full dataset
3. Applications on a random sample of the dataset preserving the ratio of anomalies
4. Applications on a balanced dataset

In approaches 1, 2, and 3, observations with air leaks were treated as anomalies due to the extremely small number; three anomaly detection techniques were applied:
1. Clustering-based: K-Means clustering using the Euclidean distance, Hierarchical clustering using different linkage measures, and Spectral Clustering
2. Distance-based: distance to the fifth-nearest neighbor using the Euclidean distance, Mahalanobis distance, and BACON
3. Density-based approaches: DBSCAN: Density-Based Spatial Clustering of Applications with Noise
   
In approach 4, instances with air leaks are no longer considered anomalies as they constitute half of the data; two techniques were used:
1. Clustering: K-Means clustering using the Euclidean distance, Hierarchical clustering using different linkage measures, and Spectral Clustering
2. Machine learning classifiers: Random Forests, K-NN, Logistic Regression, SVM, Least Squares, and Perceptron.

It is worth noting that using machine learning classifiers in the first 3 approaches (on imbalanced datasets) would have had very weak performance since the models would be biased as a result of the extreme data imbalance.
