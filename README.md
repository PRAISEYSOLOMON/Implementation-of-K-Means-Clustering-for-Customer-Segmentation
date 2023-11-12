# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries .
2. Read the data frame using pandas.
3. Get the information regarding the null values present in the dataframe.
4. Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5. Determine training and test data set.
6. Apply k means clustering for customer segmentation.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: PRAISEY S
RegisterNumber:  212222040117

import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]   #Within-Cluster Sum of Squares.

for i in range(1,11):
    kmeans=KMeans(n_clusters=i, init="k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
    
plt.plot(range(1,11),wcss)
plt.xlabel("No.of Clusters")
plt.ylabel("wcss")
plt.title("ELBOW METHOD GRAPH")
plt.show()
km = KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="green",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="purple",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="blue",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="gold",label="cluster4")
plt.legend()
plt.title("Customer Segments")

*/
```

## Output:

data.head()

![out 8 1](https://github.com/PRAISEYSOLOMON/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119394259/a3bc52ca-a31f-4afc-acf9-ae7ba9b4d36f)

data.info()

![out 8 2](https://github.com/PRAISEYSOLOMON/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119394259/c43f6f4e-fc4c-46d0-9070-c5438117cd29)

data.isnull().sum()

![out 8 3](https://github.com/PRAISEYSOLOMON/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119394259/7efb5f74-9072-4e47-8e03-5cd313d3ea39)

Elbow Method Graph

![out 8 4](https://github.com/PRAISEYSOLOMON/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119394259/1b97616a-3bf0-4e8f-bd12-9e4bc2be5f4c)

KMeans Clusters

![out 8 5](https://github.com/PRAISEYSOLOMON/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119394259/870ffc5a-d6fe-42b5-9644-d8c61417e2d8)

Y_pred

![out 8 6](https://github.com/PRAISEYSOLOMON/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119394259/aaf40515-67d9-40cf-b855-8149a2aeb7de)

Customers Segments Graph

![out 8 7](https://github.com/PRAISEYSOLOMON/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119394259/e9f08471-bc3a-4107-ad4d-03d4ddd5f9e7)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
