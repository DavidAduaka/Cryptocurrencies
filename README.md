# Cryptocurrencies - Unsuprervised Machine Learning by David Aduaka 

## Overview of the Challenge

Martha is a senior manager for the Advisory Services Team at Accountability Accounting, a prominent investment bank. Accountability Accounting is interested in offering a new cryptocurrency investment portfolio for its customers. The companies knowledge of cryptocurrencies is zero to none. They've asked for a report to be created that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system.

Unsupervised machine learning is useful for this purpose, since we don't know the output and since we want to create a classification system. In the challenge, I will first pre-process the data to fit the machine learning models using PCA. I will employ KMeans to cluster the cryptocurrencies, and then create visualizations using plotly.express and hvplot that can easily depict the different groups.

## Resources
- Data Source: crypto_data.csv
- Software: Anaconda 4.10.1, kernels mlenv, plotly.express, hvplot, PCA and KMeans libraries; Jupyter Notebook

## Results 
After pre-processing the data from the csv file, I determined that there are 532 tradable cryptocurrencies.

### Elbow Curve 
![image](https://user-images.githubusercontent.com/70069730/153332213-a343f57f-14d2-4e4a-8547-af827d21b624.png)

The elbow curve shows that inertia significantly drops up to k=4, after which there are diminishing drops for each subsequent k value. I use k=4 to create 4 classes in which to categorize the data into the following DataFrame.

![image](https://user-images.githubusercontent.com/70069730/153332409-c40ef24d-f17a-4ff8-b417-40bc77c09075.png)

### 3D Scatter with Clusters
![image](https://user-images.githubusercontent.com/70069730/153332488-97673929-6004-47fd-a7a0-ff77c4ee39fe.png)

This is a 3D visualization of the above DataFrame.

### Tradable Crypto Table
![image](https://user-images.githubusercontent.com/70069730/153332605-b7a8f5d3-3263-46ff-a06c-aedcd5d5b6e7.png)

Using hvplot, this interactive table can be created and used to further visualize the cryptocurrencies and classes. I sorted the classes in ascending order, and saw that there is only one cryptocurrency in class 3, which is BitTorrent.

### ScatterPlot of the Total Coins Mined v Total Supply
![image](https://user-images.githubusercontent.com/70069730/153332686-4348c2e9-dc7b-4ec7-85a3-df916ccfa038.png)

This scatterplot compares the Total Coins Mined versus the Total Supply. Most of the data is aggregated around the x and y axis intersection with some outliers, implying there are many cryptocurrencies with low mining and low supply.




