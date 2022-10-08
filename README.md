# Cryptocurrencies
## Table of Contents
- [Overview of the Analysis](#overview-of-the-analysis)
    - [Purpose](#purpose)
    - [About the Dataset](#about-the-dataset)
    - [Tools Used](#tools-used)
    - [Description](#description)
- [Results](#results)
    - [Preprocessing the Data for PCA](#preprocessing-the-data-for-pca)
    - [Reducing Data Dimensions Using PCA](#reducing-data-dimensions-using-pca)
    - [Clustering Cryptocurrencies Using K-Means](#Clustering-Cryptocurrencies-Using-K-Means)
    - [Visualizing Cryptocurrencies Results](#Visualizing-Cryptocurrencies-Results)
- [Summary](#summary)
- [Contact Information](#contact-information)

## Overview of the Analysis
### Purpose:
The purpose of this analysis is to aid an investment bank in offering a cryptocurrency investment portfolio to its customers. The bank seeks to find out which cryptocurrencies are available on the trading market and how they can be best grouped together, to create a classification system for this new investment portfolio.

## About the Dataset:
The dataset is in a csv file, [crypto_data.csv](). It contains data on different cryptocurrencies. 

### Tools Used:
- Python (Scikit-learn, Plotly, hvPlot, and Pandas libraries)

### Description:
This analysis ventures to report the different cryptocurrencies present on the trading market, and how these can be grouped to create a classification system for a new investment by the clients. Since we are taking in raw data and do not have known outcomes for what we are looking for, we apply an unsupervised machine learning model on the input data. The data is preprocessed, undergoes dimensionality reduction using PCA (Principal Components Analysis), and is then clustered using a clustering algorithm - the K-Means algorithm. Lastly, the results are visualized.

## Results
### Preprocessing the Data for PCA

![crypto_df](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/crypto_df.png)

A crypto_df is created by removing the columns not needed and null values in the data. The features are then standardized before running PCA.

### Reducing Data Dimensions Using PCA
The dimensions are reduced to only 3: "PC 1", "PC 2", and "PC 3", as shown below:

![pcs_df](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/pcs_df.png)

### Clustering Cryptocurrencies Using K-Means
An elbow curve is created in order to determine the best value for K, by iterating on k values in range(1,11) (i.e. from 1 to 10). The best K value seems to be 4 since there is a sharper horizontal slant to the slope after this value. The K-means algorithm is then run to predict the K clusters for the cryptocurrencies. A K value of 4 means that the output will have 4 clusters wherein the cryptocurrencies will have been clustered. 

![elbow_curve](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/elbow_curve.png)

Another table is created by concatenating the crypto_df and pcs_df:

![clustered_df](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/clustered_df.png)

### Visualizing Cryptocurrencies Results
A 3d-scatter plot is created to visualize the distinct groups that correspond to the three principal components. Dimesionlaity reduction results in 3 principal components. 

![3d scatter plot](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/3d_scatter_plot.png)

A 2d-scatter plot is created to visualize all the currently tradable cryptocurrencies. Dimesionlaity reduction results in 2 principal components. 

![2d scatter plot](https://github.com/SohaT7/Cryptocurrencies/blob/main/Images/2d_scatter_plot.png)

In both these scatter plots, the outlier (i.e. class 2) is clearly visible.

## Summary
There are 532 tradable cryptocurrencies, which were classified based on the similarities in their features. Each resultant group can be analyzed further to determine exactly how viable investing in each group of cryptocurrencies will prove for the clients. 

## Contact Information
Email: st.sohatariq@gmail.com

