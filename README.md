# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Start the program.

2.Import required libraries like pandas, matplotlib, and sklearn.

3.Load the Mall_Customers.csv dataset.

4.Select Annual Income and Spending Score as features.

5.Initialize an empty list to store WCSS values.

6.Apply K-Means for cluster values from 1 to 10.

7.Store inertia (WCSS) for each cluster value.

8.Plot the Elbow graph to find the optimal number of clusters.

9.Train K-Means again using the chosen number of clusters (e.g., 5).

10.Predict clusters, assign them to customers, and visualize the clusters using scatter plot


## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: K Lokesh Achari
RegisterNumber: 25012708

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
data = pd.read_csv("Mall_Customers.csv")
X = data[['Annual Income (k$)', 'Spending Score (1-100)']]
print(data.head())
kmeans = KMeans(n_clusters=5, random_state=42)
y_kmeans = kmeans.fit_predict(X)

data['Cluster'] = y_kmeans

print("\nClustered Data:")
print(data.head())

plt.figure()
plt.scatter(X[y_kmeans == 0]['Annual Income (k$)'], 
            X[y_kmeans == 0]['Spending Score (1-100)'], label='Cluster 0')

plt.scatter(X[y_kmeans == 1]['Annual Income (k$)'], 
            X[y_kmeans == 1]['Spending Score (1-100)'], label='Cluster 1')

plt.scatter(X[y_kmeans == 2]['Annual Income (k$)'], 
            X[y_kmeans == 2]['Spending Score (1-100)'], label='Cluster 2')

plt.scatter(X[y_kmeans == 3]['Annual Income (k$)'], 
            X[y_kmeans == 3]['Spending Score (1-100)'], label='Cluster 3')

plt.scatter(X[y_kmeans == 4]['Annual Income (k$)'], 
            X[y_kmeans == 4]['Spending Score (1-100)'], label='Cluster 4')

plt.scatter(kmeans.cluster_centers_[:,0], 
            kmeans.cluster_centers_[:,1], 
            s=200, label='Centroids')

plt.title("Customer Segmentation using K-Means")
plt.xlabel("Annual Income (k$)")
plt.ylabel("Spending Score (1-100)")
plt.legend()
plt.show()



```

## Output:
<img width="999" height="792" alt="Screenshot 2026-02-27 105927" src="https://github.com/user-attachments/assets/8385c301-aaae-4513-9678-b33dfe55c09a" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
