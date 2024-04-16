# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
```
1.Import the necessary packages using import statement.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Import KMeans and use for loop to cluster the data.

4.Predict the cluster and plot data graphs.

5.Print the outputs and end the program
```
```

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: sreenithi.E
RegisterNumber:  212223220109
*/
```
```
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
  kmeans = KMeans (n_clusters = i, init ="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("no of cluster")
plt.ylabel("wcss")
plt.title("Elbow Metthod")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="pink",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="green",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="blue",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="black",label="cluster4")
plt.legend()
plt.title("Customer Segments")
```
``


## Output:
```
```
Datahead

![image](https://github.com/sreenithi23/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147017600/3e7799bb-e23a-4fc1-888f-57aecbb52dee)

Info

![image](https://github.com/sreenithi23/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147017600/f90dfcf6-9027-438b-97d7-b13a9cc411f6)

Total Rows

![image](https://github.com/sreenithi23/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147017600/3d974e40-2db6-4838-85b9-99a9ffb9dbaa)



Plot for Elbow Method

![image](https://github.com/sreenithi23/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147017600/61e9da3e-7a9d-45a9-bc5f-02c01e4bb369)

K-Means Clustering

![image](https://github.com/sreenithi23/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147017600/b1c2cb10-cdf7-44a5-b3bb-510b28fb3229)

y_Pred

![image](https://github.com/sreenithi23/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147017600/3b599ed9-1ab8-4f7e-811c-7b319ec9bca6)



Plot for customer Segements

![image](https://github.com/sreenithi23/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147017600/ad89d4ab-99d3-4bf1-a45b-6633a48b67d0)





## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
