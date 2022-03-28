# Cryptocurrency Clusters
The aim of this project is to determine cryptocurrencies grouping based upon unsupervised machine learning. The project will compare clustering algorithms, such as Kmeans, Hierachical Clustering. 
## Objectives
The goals for this project is to:

* Prepare the data for dimensions reduction with PCA and clustering using K-means.
* Reduce data dimensions using PCA algorithms from sklearn.
* Predict clusters using cryptocurrencies data using the K-means algorithm form sklearn.
* Create some plots and data tables to present the results.


## Technologies Used
* Python
* Jupyter Notebook
* Pandas
* Sklearn (StandardScaler, PCA, AgglomerativeClustering, KMeans)


## Processes

### Data Preprocessing
* Remove all cryptocurrencies that aren’t trading.
* Remove all cryptocurrencies that don’t have an algorithm defined.
* Remove the IsTrading column.
* Remove all cryptocurrencies with at least one null value.
* Remove all cryptocurrencies without coins mined.
* Store the names of all cryptocurrencies on a DataFramed named coins_name, and use the crypto_df.index as the index for this new DataFrame.
* Remove the CoinName column.
* Create dummies variables for all of the text features, and store the resulting data on a DataFrame named X.
* Use the StandardScaler from sklearn (Links to an external site.) to standardize all of the data from the X DataFrame. This is important prior to * using PCA and K-means algorithms.

### Reducing Data Dimensions Using PCA
* Use the PCA algorithm from sklearn (Links to an external site.) to reduce the dimensions of the X DataFrame down to three principal components.
* After reducing the data dimensions, create a DataFrame named “pcs_df” that includes the following columns: PC 1, PC 2, and PC 3. Use the crypto_df.index as the index for this new DataFrame.

### Clustering Cryptocurrencies Using K-means
* Create an elbow curve to find the best value for K, and use the pcs_df DataFrame.
* Run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data. Use the pcs_df to run the K-means algorithm.
* Create a new DataFrame named “clustered_df,” that includes the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class. Remember to maintain the index of the crypto_df DataFrames as is shown below
### Summary
I discarded from the dataframe all cryptocurrencies that are not being traded, dropped rows that contain null values, filter the dataframe for cryptocurrencies that have been mined, dummy variables are created for the Algorithm and ProofType columns and the data is standardized with StandardScaler.

When it comes to dimensionality reduction, I created a PCA model, model's explained variance is set to 90% (0.9), the shape of the reduced dataset is examined, t-SNE model is created and used to reduce dimensions and t-SNE is used to create a plot of the reduced features.

And finally for the cluster analysis and conclusion, k-means model was used, a for loop is used to create a list of inertias for each K from 1 to 10, inclusive, a plot is created to examine any elbows and your conclusion is appropriate based on your own findings. 
