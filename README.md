<h1>Module 19 Challenge: Crypto Clustering</h1>

<h2>Background</h2>
<p>In this challenge, you’ll use your knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.</p>

<h2>Requirements</h2>

<h3>1. Find the Best Value for k by Using the Original Data</h3>

- Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.

- To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.

  ![image](https://github.com/user-attachments/assets/1a09cd2d-742c-4b3f-ab24-3cb9562d22a6)

- Answer the following question: What’s the best value for k?

  <pre><strong>Answer:</strong>The best value for k appears to be 4. </pre>

<h3>2. Cluster the Cryptocurrencies with K-Means by Using the Original Data</h3>

- Initialize the K-means model with four clusters by using the best value for k.

- Fit the K-means model by using the original data.

- Predict the clusters for grouping the cryptocurrencies by using the original data. Review the resulting array of cluster values.

- Create a copy of the original data, and then add a new column of the predicted clusters.

- Using hvPlot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d".
  
- Color the graph points with the labels that you found by using K-means.
  
- Add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents.

  ![image](https://github.com/user-attachments/assets/6673d5cf-c6e2-4dc1-9a53-54b70be070dc)

<h3>3. Optimize the Clusters with Principal Component Analysis</h3> 

- Create a PCA model instance, and set n_components=3. 

- Use the PCA model to reduce the features to three principal components. Then review the first five rows of the DataFrame.

- Get the explained variance to determine how much information can be attributed to each principal component.

  ![image](https://github.com/user-attachments/assets/c76b6c41-065d-47bc-a706-2acafc66aee3)

- Answer the following question: What’s the total explained variance of the three principal components?

  <pre><strong>Answer:</strong>The total explained variance for all theree principal components is 0.89503166 or roughly 90%. </pre>

- Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.

<h3>4. Find the Best Value for k by Using the PCA Data</h3>

- Code the elbow method algorithm, and use the PCA data to find the best value for k. Use a range from 1 to 11. 

- To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.

  ![image](https://github.com/user-attachments/assets/8cf30569-1f82-42c9-857b-0e4b2dac11af)

- Answer the following questions: What’s the best value for k when using the PCA data? Does it differ from the best value for k that you found by using the original data?

  <pre><strong>Answer:</strong>The best value for k when using PCA data is 4. This is the same as the best value for k that was found using the original data.</pre>

<h3>5. Cluster the Cryptocurrencies with K-means by Using the PCA Data</h3>

- Initialize the K-means model with four clusters by using the best value for k.

- Fit the K-means model by using the PCA data.

- Predict the clusters for grouping the cryptocurrencies by using the PCA data.
  
- Review the resulting array of cluster values.

- Create a copy of the DataFrame with the PCA data, and then add a new column to store the predicted clusters. 

- Using hvPlot, create a scatter plot by setting x="PC1" and y="PC2".
  
- Color the graph points with the labels that you found by using K-means.
  
- Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents.

  ![image](https://github.com/user-attachments/assets/06f5f44c-0355-41cf-9161-e50b814db901)

<h3>6. Visualize and Compare the Results</h3>

- Create a composite plot by using hvPlot and the plus sign (+) operator to compare the elbow curve that you created from the original data with the one that you created from the PCA data.

- Create a composite plot by using hvPlot and the plus (+) operator to compare the cryptocurrency clusters that resulted from using the original data with those that resulted from the PCA data.

  ![image](https://github.com/user-attachments/assets/fd956e17-7ff8-42f9-9ff7-53a49847bc56)

  ![image](https://github.com/user-attachments/assets/4c5577b1-b4b4-47d6-b25a-7d0437d0672f)

- Answer the following question: Based on visually analyzing the cluster analysis results, what’s the impact of using fewer features to cluster the data by using K-means?

  <pre><strong>Answer:</strong>Both the original data using K-means and the PCA data showed the optimal number of clusters to be 4.</pre>

<h3>7. Coding Conventions and Formatting</h3>

- Place imports at the top of the file, just after any module comments and docstrings, and before module globals and constants.

- Name functions and variables with lowercase characters, with words separated by underscores.

- Follow DRY (Don't Repeat Yourself) principles, creating maintainable and reusable code.

- Use concise logic and creative engineering where possible.

<h3>8. Deployment and Submission</h3>

- Submit a link to a GitHub repository that’s cloned to your local machine and that contains your files.

- Use the command line to add your files to the repository.

- Include appropriate commit messages in your files.

<h3>9. Code Comments</h3>

- Be well commented with concise, relevant notes that other developers can understand.
