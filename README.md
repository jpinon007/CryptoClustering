# CryptoClustering

# Background: In this challenge, I used my knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. In order to complete this assignment, I checked my code using someone else's work for reference https://github.com/JLeigh101/CryptoClustering.git

# Solution: I used the StandardScaler() module from scikit-learn to normalize the data from the CSV file. I created a dataframe with the scaled data and set the "coin_id" index from the original DataFrame as the indez for the new DataFrame. I was then asked to use the elbow method to find the best value for k using the following steps; create a list with the number of k values from 1 to 11, create an empty list to store the inertia values, create a for loop to compute the inertia with each possible value of k, create a dictionary with the data to plot the elbow curve, plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k, and answer the following question in my notebook: What is the best value for k?

# Next I was asked to cluster the cryptocurrencies for the  best value for k on the scaled DataFrame using the following steps; Initialize the K-means model with the best value for k, fit the K-means model using the scaled DataFrame, predict the clusters to group the cryptocurrencies using the scaled DataFrame, create a copy of the scaled DataFrame and add a new column with the predicted clusters, create a scatter plot using hvPlot as follows: set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d", color the graph points with the labels found using K-means, and add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

# Optimize Clusters with Principal Component Analysis: using the original scaled DataFrame, I performed a PCA and reduced the features to three principal components. I had to retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the question "What is the total explained variance of the three princiapl components?", and finally created a new DataFrames with the scaled PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame. 

# Fine