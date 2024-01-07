# cryptoclustering

# Cryptocurrency Clustering with K-Means and PCA

## Introduction

This project involves clustering cryptocurrencies using the K-Means algorithm and Principal Component Analysis (PCA). The goal is to explore the impact of using different feature sets on the clustering results.

## Preparation of the Data

### Normalization with StandardScaler

Use the `StandardScaler()` module from scikit-learn to normalize the data from the CSV file. Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

### Finding the Best Value for k

Use the elbow method to find the best value for k with the original scaled DataFrame:

1. Create a list with the number of k values from 1 to 11.
2. Create an empty list to store the inertia values.
3. Use a for loop to compute the inertia with each possible value of k.
4. Create a dictionary with the data to plot the elbow curve.
5. Plot a line chart with all the inertia values to visually identify the optimal value for k.

Answer the question: What is the best value for k?

### Clustering Cryptocurrencies with K-Means Using Original Scaled Data

1. Initialize the K-means model with the best value for k.
2. Fit the K-means model using the original scaled DataFrame.
3. Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
4. Create a copy of the original data and add a new column with the predicted clusters.
5. Create a scatter plot using hvPlot to visualize the clusters.

### Optimizing Clusters with Principal Component Analysis

1. Perform PCA on the original scaled DataFrame and reduce features to three principal components.
2. Retrieve the explained variance to determine the total explained variance of the three principal components.

Answer the question: What is the total explained variance of the three principal components?

3. Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Finding the Best Value for k Using PCA Data

Use the elbow method on the PCA data to find the best value for k:

1. Create a list with the number of k-values from 1 to 11.
2. Create an empty list to store the inertia values.
3. Use a for loop to compute the inertia with each possible value of k.
4. Create a dictionary with the data to plot the elbow curve.
5. Plot a line chart with all the inertia values to visually identify the optimal value for k.

Answer the question: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?

### Clustering Cryptocurrencies with K-Means Using PCA Data

1. Initialize the K-means model with the best value for k.
2. Fit the K-means model using the PCA data.
3. Predict the clusters to group the cryptocurrencies using the PCA data.
4. Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
5. Create a scatter plot using hvPlot to visualize the clusters.

Answer the question: What is the impact of using fewer features to cluster the data using K-Means?


