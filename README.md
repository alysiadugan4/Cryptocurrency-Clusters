# Cryptocurrency Clusters

## Background

- You are on the Advisory Services Team of a financial consultancy. One of your clients, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. They’ve asked you to create a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for this new investment.
- You have been handed raw data, so you will first need to process it to fit the machine learning models. Since there is no known classification system, you will need to use unsupervised learning. You will use several clustering algorithms to explore whether the cryptocurrencies can be grouped together with other similar cryptocurrencies. You will use data visualization to share your findings with the investment bank.

## Instructions

### Data Preparation

- In order for your dataset to be comprehensible to a machine learning algorithm, its data should be numeric. Since the coin names do not contribute to the analysis of the data, delete the `CoinName` from the original dataframe.
- Convert the remaining features with text values, `Algorithm` and `ProofType`, into numerical data. 
- Standardize your dataset so that columns that contain larger values do not unduly influence the outcome.

### Dimensionality Reduction

- Creating dummy variables above dramatically increased the number of features in your dataset. Perform dimensionality reduction with PCA. For this project, preserve 90% of the explained variance in dimensionality reduction.
- Next, further reduce the dataset dimensions with t-SNE and visually inspect the results. Then create a scatter plot of the t-SNE output. Observe whether there are distinct clusters or not.

### Cluster Analysis with k-Means

- Create an elbow plot to identify the best number of clusters. Determine, if possible, where the elbow of the plot is, and at which value of `k` it appears.

## Summary

To tackle this project of determining if cryptocurrencies can be clustered for the purposes of investing, I started with data cleanup. I removed any currencies that were not currently trading, as well as those that had null values in any of the columns. I also filtered for coins that had been mined. 


The next step was to do some basic formatting, removing unnecessary columns and converting all fields to numeric values. I also used get_dummies to fill in any missing fields and standardized the data to nullify outliers.


Next, I used PCA to reduce the dimensionality to 90% of the explained variance, then t-SNE to reduce it further to a learning rate of 250. To test, I used a scatter plot to see if any clusters were observable. At a glance, there do appear to be some clusters. 


Using k-means, I analyzed the clusters further. The resulting graph is a fairly straight downward diagonal line, suggesting that there likely aren't any true clusters. This could perhaps be refined by removing additional outliers to get closer to the 1-2 clusters that were visible in the scatter plot.


