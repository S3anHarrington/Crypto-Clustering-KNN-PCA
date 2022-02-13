## Crypto-Clustering

In this Challenge, you’ll combine your financial Python programming skills with the new unsupervised learning skills that you acquired in this module.

The CSV file provided for this challenge contains price change data of cryptocurrencies in different periods.

The steps for this challenge are broken out into the following sections:

Import the Data (provided in the starter code)
Prepare the Data (provided in the starter code)
Find the Best Value for k Using the Original Data
Cluster Cryptocurrencies with K-means Using the Original Data
Optimize Clusters with Principal Component Analysis
Find the Best Value for k Using the PCA Data
Cluster the Cryptocurrencies with K-means Using the PCA Data
Visualize and Compare the Results
Import the Data

This section imports the data into a new DataFrame. It follows these steps:

Read the “crypto_market_data.csv” file from the Resources folder into a DataFrame, and use index_col="coin_id" to set the cryptocurrency name as the index. Review the DataFrame.

Generate the summary statistics, and use HvPlot to visualize your data to observe what your DataFrame contains.

Rewind: The Pandasdescribe()function generates summary statistics for a DataFrame.

## Import the Data

This section imports the data into a new DataFrame. It follows these steps:

Read the “crypto_market_data.csv” file from the Resources folder into a DataFrame, and use index_col="coin_id" to set the cryptocurrency name as the index. Review the DataFrame.

Generate the summary statistics, and use HvPlot to visualize your data to observe what your DataFrame contains.

Rewind: The Pandasdescribe()function generates summary statistics for a DataFrame.

![Screen Shot 2022-02-13 at 13 32 29](https://user-images.githubusercontent.com/91238235/153775951-e9a67b9d-bc3a-4c2a-a178-abe25f468427.png)

![Screen Shot 2022-02-13 at 13 33 36](https://user-images.githubusercontent.com/91238235/153775984-35211da2-8dad-4254-881c-d15f738ada31.png)

![Screen Shot 2022-02-13 at 13 34 12](https://user-images.githubusercontent.com/91238235/153776004-31c21d33-9784-4475-b438-e81c8c97febd.png)

![Screen Shot 2022-02-13 at 13 34 49](https://user-images.githubusercontent.com/91238235/153776037-5d7aee9d-d1ab-44c6-871e-a0668e4260cb.png)


## Prepare the Data

This section prepares the data before running the K-Means algorithm. It follows these steps:

Use the StandardScaler module from scikit-learn to normalize the CSV file data. This will require you to utilize the fit_transform function.

Create a DataFrame that contains the scaled data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.

![Screen Shot 2022-02-13 at 13 36 33](https://user-images.githubusercontent.com/91238235/153776111-acd9bc05-240a-44e9-a80a-f2237ba2cd0b.png)


## Find the Best Value for k Using the Original Data

In this section, you will use the elbow method to find the best value for k.

Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.

Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

Answer the following question: What is the best value for k?

![Screen Shot 2022-02-13 at 13 37 40](https://user-images.githubusercontent.com/91238235/153776154-3b64b5d0-1c71-4629-8243-d4aefe6ffa7c.png)

![Screen Shot 2022-02-13 at 13 38 12](https://user-images.githubusercontent.com/91238235/153776174-f450c86c-ebef-400e-b6b7-81421ab92b5b.png)

Answer the following question: What is the best value for k?

Question: What is the best value for k?

Answer: 4

## Cluster Cryptocurrencies with K-means Using the Original Data

In this section, you will use the K-Means algorithm with the best value for k found in the previous section to cluster the cryptocurrencies according to the price changes of cryptocurrencies provided.

Initialize the K-Means model with four clusters using the best value for k.

Fit the K-Means model using the original data.

Predict the clusters to group the cryptocurrencies using the original data. View the resulting array of cluster values.

Create a copy of the original data and add a new column with the predicted clusters.

Create a scatter plot using hvPlot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Color the graph points with the labels found using K-Means and add the crypto name in the hover_cols parameter to identify the cryptocurrency represented by each data point.

![Screen Shot 2022-02-13 at 13 40 48](https://user-images.githubusercontent.com/91238235/153776263-0135ec58-0a13-48a6-a526-e8a1b684c3d3.png)

![Screen Shot 2022-02-13 at 13 41 19](https://user-images.githubusercontent.com/91238235/153776279-b876aebe-e1c2-4d32-91a3-81c0e3c1c54f.png)

![Screen Shot 2022-02-13 at 13 41 48](https://user-images.githubusercontent.com/91238235/153776309-d610aed7-ecb2-4de3-9163-7a00dd738b1b.png)

## Optimize Clusters with Principal Component Analysis

In this section, you will perform a principal component analysis (PCA) and reduce the features to three principal components.

Create a PCA model instance and set n_components=3.

Use the PCA model to reduce to three principal components. View the first five rows of the DataFrame.

Retrieve the explained variance to determine how much information can be attributed to each principal component.

Answer the following question: What is the total explained variance of the three principal components?

Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.

![Screen Shot 2022-02-13 at 13 42 53](https://user-images.githubusercontent.com/91238235/153776350-82ce59d2-e2fe-4c42-a48e-9bf5a02ceab1.png)

Answer the following question: What is the total explained variance of the three principal components?

Question: What is the total explained variance of the three principal components?

Answer: 89.5%

![Screen Shot 2022-02-13 at 13 43 44](https://user-images.githubusercontent.com/91238235/153776378-31ed2de5-a139-4d54-8a35-8cf1475dc098.png)

## Find the Best Value for k Using the PCA Data

In this section, you will use the elbow method to find the best value for k using the PCA data.

Code the elbow method algorithm and use the PCA data to find the best value for k. Use a range from 1 to 11.

Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

Answer the following questions: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?

![Screen Shot 2022-02-13 at 13 44 53](https://user-images.githubusercontent.com/91238235/153776411-1c10de12-72a5-4d90-9315-9accd6416639.png)

![Screen Shot 2022-02-13 at 13 45 19](https://user-images.githubusercontent.com/91238235/153776425-71b8ef04-730a-444b-8a07-7b497f6425f1.png)

![Screen Shot 2022-02-13 at 13 45 47](https://user-images.githubusercontent.com/91238235/153776436-5c589a99-9594-441e-96a4-7d0705a45337.png)

Answer the following questions: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?

Question: What is the best value for k when using the PCA data?

Answer: 4
Question: Does it differ from the best k value found using the original data?

Answer: No, the best k value does not change. However, 4 has dropped 25 points on the inertia scale.

## Cluster Cryptocurrencies with K-means Using the PCA Data

In this section, you will use the PCA data and the K-Means algorithm with the best value for k found in the previous section to cluster the cryptocurrencies according to the principal components.

Initialize the K-Means model with four clusters using the best value for k.

Fit the K-Means model using the PCA data.

Predict the clusters to group the cryptocurrencies using the PCA data. View the resulting array of cluster values.

Add a new column to the DataFrame with the PCA data to store the predicted clusters.

Create a scatter plot using hvPlot by setting x="PC1" and y="PC2". Color the graph points with the labels found using K-Means and add the crypto name in the hover_cols parameter to identify the cryptocurrency represented by each data point.

![Screen Shot 2022-02-13 at 13 47 23](https://user-images.githubusercontent.com/91238235/153776509-e824b91d-65e0-4397-9a39-be19ce8060a6.png)

![Screen Shot 2022-02-13 at 13 48 33](https://user-images.githubusercontent.com/91238235/153776528-66452ca6-5a80-402d-80cd-27971df17e7d.png)

![Screen Shot 2022-02-13 at 13 48 58](https://user-images.githubusercontent.com/91238235/153776574-125744dc-f407-4f84-b660-1dbbb466646a.png)

## Visualize and Compare the Results

In this section, you will visually analyze the cluster analysis results by contrasting the outcome with and without using the optimization techniques.

Create a composite plot using hvPlot and the plus (+) operator to contrast the Elbow Curve that you created to find the best value for k with the original and the PCA data.

Create a composite plot using hvPlot and the plus (+) operator to contrast the cryptocurrencies clusters using the original and the PCA data.

Answer the following question: After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?

Rewind: Back in Lesson 3 of Module 6, you learned how to create composite plots. You can look at that lesson to review how to make these plots; also, you can check the hvPlot documentation.

![Screen Shot 2022-02-13 at 13 50 19](https://user-images.githubusercontent.com/91238235/153776639-90adf220-715e-4854-976e-7d0ef8693232.png)

![Screen Shot 2022-02-13 at 13 50 53](https://user-images.githubusercontent.com/91238235/153776663-e0292b95-a81e-47bf-9204-66181a699c58.png)

Answer the following question: After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?

Answer: It elimiates some of the outliers, allowing the data to be cleaned up and present a more accurate depiction of the cluster.
