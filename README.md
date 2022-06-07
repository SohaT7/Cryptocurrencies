# Cryptocurrencies
## Overview of the Analysis
### Purpose
The purpose of this analysis was to aid our clients at Accountability Accounting in deciding if, and how, they will be breaking into the cryptocurrency market. 

### Description
This analysis ventures to report the different cryptocurrencies present on the trading market, and how these can be grouped to create a classification system for the new investment by the clients. Since we are taking in raw data and do not know the outcomes, we apply an unsupervised machine learning model on the input data. This involved preprocessing the data, dimensionality reduction using PCA (Principal Components Analysis), clustering using K-Means algorithm, and lastly visualizing the cryptocurrencies results.

## Results
### (1) Preprocessing the Data for PCA

![crypto_df](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/crypto_df.png)

A crypto_df is created by removing the columns not needed and null values in the data. The features are then standardized before running PCA.

### (2) Reducing Data Dimensions Using PCA
The dimensions are reduced to only 3: "PC 1", "PC 2", and "PC 3", as shown below:

![pcs_df](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/pcs_df.png)

### (3) Clustering Cryptocurrencies Using K-Means
An elbow curve is created in order to determine the best value for K, by iterating on k values in range(1,11) (i.e. from 1 to 10). The best K value seems to be 4 since there is a sharper horizontal slant to the slope after this value. The K-means algorithm is then run to predict the K clusters for the cryptocurrencies. A K value of 4 means that the output will have 4 clusters wherein the cryptocurrencies will have been clustered. 

![elbow_curve](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/elbow_curve.png)

Another table is created by concatenating the crypto_df and pcs_df:

![clustered_df](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/clustered_df.png)

### (4) Visualizing Cryptocurrencies Results
A 3d-scatter plot is created to visualize the distinct groups that correspond to the three principal components. Dimesionlaity reduction results in 3 principal components. 

![3d scatter plot](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/3d_scatter_plot.png)

A 2d-scatter plot is created to visualize all the currently tradable cryptocurrencies. Dimesionlaity reduction results in 2 principal components. 

![2d scatter plot](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/2d_scatter_plot.png)

In both these scatter plots, the outlier (i.e. class 2) is clearly visible.

## Summary
There are 532 tradable cryptocurrencies, which we classified based on the similarities in their features. Each resultant group can be analyzed further to determine how viable investing in each group of cryptocurrencies will prove for the clients. 


