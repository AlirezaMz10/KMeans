# KMeans Clustering Implementation

This repository contains a Python implementation of the KMeans clustering algorithm. The KMeans algorithm is used for clustering data points into a predefined number of clusters based on similarity. This implementation includes visualization for both 2D and 3D datasets using `matplotlib`.

## Features
- Loads a dataset (Iris dataset in this case) from a CSV file.
- Implements the KMeans algorithm to cluster data points into a specified number of clusters.
- Supports visualization for 2D and 3D data points.
- Includes an example using the Iris dataset to demonstrate the clustering functionality.

## Dependencies
- `numpy`: For numerical operations and handling arrays.
- `matplotlib`: For data visualization.
  
To install the required dependencies, you can use the following command:


```
pip install numpy matplotlib
```

## Usage

1.	Clone this repository to your local machine:

```
git clone https://github.com/AlirezaMz10/KMeans.git
cd KMeans
```

2.	Make sure you have the iris.csv file in the correct directory or provide the correct path to the dataset.

https://gist.github.com/netj/8836201


3.	Run the Python script to perform KMeans clustering:


## Code Explanation

- The script loads the Iris dataset from a CSV file (iris.csv).
  
- 	The KMeans class implements the core KMeans clustering algorithm with a method fit() that clusters the data points and visualizes the results.
  
-	The script uses matplotlib to plot the 2D or 3D scatter plot based on the data dimensions.

## Example

```
import numpy as np
import matplotlib.pyplot as plt

# Load data
df = np.loadtxt("/content/iris.csv", delimiter=",", dtype=str)
sepal_length = np.array(df[1:, 0], dtype=np.float64)
sepal_width = np.array(df[1:, 1], dtype=np.float64)
petal_length = np.array(df[1:, 2], dtype=np.float64)
petal_width = np.array(df[1:, 3], dtype=np.float64)

# Data preparation
A = np.array([sepal_length, sepal_width, petal_length]).T

# KMeans clustering
kmeans = KMeans(A, n_clusters=3)
clusters, labels = kmeans.fit()