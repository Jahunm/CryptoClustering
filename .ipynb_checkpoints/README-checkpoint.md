# Module 10 Application - Crypto Clustering

---

   ![Coins](Images/CryptoCoins.png)

You’ll assume the role of an advisor in one of the top five financial advisory firms in the world. Competitors are fierce, so you want to propose a novel approach to assembling investment portfolios that are based on cryptocurrencies. Instead of basing your proposal on only returns and volatility, you want to include other factors that might impact the crypto market—leading to better performance for your portfolio.

When you present the idea, your manager loves it! So, you’re asked to create a prototype for submitting your crypto portfolio proposal to the company board of directors.

---

## Table of Contents
1. [Find the Best Value for k by Using the Original Data.](#1-find-the-best-value-for-k-by-using-the-original-data)

2. [Cluster Cryptocurrencies with K-Means by Using the Original Data.](#2-cluster-cryptocurrencies-with-k-means-by-using-the-original-data)

3. [Optimize Clusters with Principal Component Analysis.](#3-coptimize-clusters-with-principal-component-analysis)

4. [Find the Best Value for k by Using the PCA Data.](#4-find-the-best-value-for-k-by-using-the-pca-data)

5. [Cluster Cryptocurrencies with K-means by Using the PCA Data.](#5-cluster-cryptocurrencies-with-k-means-by-using-the-pca-data)

6. [Visualize and Compare the Results.](#6-visualize-and-compare-the-results)

---

## 1. [Find the Best Value for k by Using the Original Data.](#1-find-the-best-value-for-k by-using-the-original-data)

Find the Best Value for k by Using the Original Data
Explore the elbow method to determine the optimal value for 'k' (number of clusters) using the original data. Code the algorithm, plot the inertia values, and identify the best 'k'.

Question: What’s the best value for 'k'?

   ![KMeans with original data](Images/OGKmeans.png)


  **Answer:** I think I would go with using 4 clusters. Thats where i notice the most dramatic change in the bell curve. However, I would probably run a try with 6 clusters because i like the where its sitting on the curve. For now, im going with 4!
      
    
## 2. [Cluster Cryptocurrencies with K-Means by Using the Original Data.](#2-cluster-cryptocurrencies-with-k-means-by-using-the-original-data)

Apply the K-means algorithm with the best 'k' to cluster cryptocurrencies based on their price changes. Visualize the results using hvPlot with a scatter plot.
   
   ![Scatter plot with 4 clusters](Images/market_scaled_plot.png)
              
## 3. [Optimize Clusters with Principal Component Analysis.](#3-coptimize-clusters-with-principal-component-analysis)

Utilize Principal Component Analysis (PCA) to reduce features to three principal components. Examine the explained variance to understand the information captured.

**Question:** What’s the total explained variance of the three principal components?
    **Answer:** # The total variance is 89.5% of the original data for analysis!
    
## 4. [Find the Best Value for k by Using the PCA Data.](#4-find-the-best-value-for-k-by-using-the-pca-data)

Repeat the elbow method, this time using PCA data. Code the algorithm, plot the inertia values, and compare the best 'k' with the one obtained from the original data.

   ![Elbow curve method with PCA data](Images/PCA_elbow.png)

* **Question:** What is the best value for `k` when using the PCA data?

  * **Answer:** I would stick with using 4 clusters...


* **Question:** Does it differ from the best k value found using the original data?

  * **Answer:** It seems very similar to me. Maybe, the elbow curve run of the PCA data seems easier to see the break in inertia


## 5. [Cluster Cryptocurrencies with K-means by Using the PCA Data.](#5-cluster-cryptocurrencies-with-k-means-by-using-the-pca-data)

Apply K-means to cluster cryptocurrencies based on PCA-transformed data. Visualize the results with a scatter plot using hvPlot.
    
   ![Scatter plot using the PCA data](Images/pca_plot.png)

## 6. [Visualize and Compare the Results.](#6-visualize-and-compare-the-results)

Compare the elbow curves and cryptocurrency clusters from the original data and PCA data. Observe the impact of using fewer features for clustering.

The Elbow curve plotted for both senarios, to determine if there is any difference in the curve. When shown side by side its very easy to see that they are virtually identical.

   ![Both Elbow curve plots side by side](Images/both_elbows.png)

Here is both scatter plots of the data side by side. Even though i am using the same amount of clusters, its is my personal opinion that the data filtered through the PCA method is clustering in a way that is much easier for me to identify with.

   ![Both scatter plots side by side](Images/both_scatters.png)
    

* **Question:** After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?

  * **Answer:** I, personally, am in the opinion that the two elbow curves are identical and let to me using 4 clusters in both senario's. However, after visualizing the Kmeans and PCA data, mind you both using the same number of clusters and same random_state, the scatter plot using the PCA data was more helpful clustering. I wish I knew how to visualize the PCA data in a 3 dimensional plot to see the true depths at which the PCA data could provide. 
    
**File:** [Clustering crypto with machine learning](crypto_investments.ipynb)    

