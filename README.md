# Crypto Clusters 

## Background
In this challenge, I use unsupervised machine learning on raw cryptocurrency data on behalf of the Advisory Services Team of a financial consultancy. An investment bank has requested a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for this new investment.


## Data Preparation	
Here are the steps I took to clean the data.

* Read `crypto_data.csv` into Pandas. 
* Discard all cryptocurrencies that are not being traded and drop the `IsTrading` column from the dataframe.
* Remove all rows that have at least one null value.
* Filter for cryptocurrencies that have been mined.
* Convert the remaining features with text values, `Algorithm` and `ProofType`, into numerical data.
* Standardize your dataset so that columns that contain larger values do not unduly influence the outcome.

## Dimensionality Reduction
The first step in machine learning is to reduce the number of features to a manageable size. Creating dummy variables above dramatically increased the number of features. I performed dimensionality reduction with PCA that explains 90% of variance.  I further reduced the dataset dimensions with t-SNE and visually inspected the results.

---
### There are 4 indistinct clusters, with one obvious outlier. 

## Cluster Analysis with k-Means
Another machine learning method is Kmeans.  I create an elbow plot to identify the best number of clusters. 

---
### The best value of 'k' is 4.

## Recommendation
It is clear from both PCA/T-SNE and Kmeans that the cryptocurrencies can be grouped into 4 categories.  Further analysis is needed to determine the performance of the crypto groups in the market.
