---
layout: post
title:  "Blog Post: Spectral Clustering"
date:   2022-2-11
categories: blog assignment
permalink: posts/blog-post-4
author: Miao Wang
---
In this blog, I will go through the whole process for how to do Spectral Clustering. It is very interesting and important for Data Science. 

**1.Prepare Data**
First step, we need to import some packages for us to use later. Numpy is an important package when we are do data analysis. Since we do not have real data 
to analyze, we will create some fake data for this tutorial. We are going to have some data which is divided into two clusters. At the end of the tutorial, we 
will learn how to separate these data into two clusters.
```python
import numpy as np
from scipy.optimize import minimize
from sklearn import datasets
from matplotlib import pyplot as plt
from sklearn.metrics import pairwise_distances
n = 200
np.random.seed(1111)
X, y = datasets.make_blobs(n_samples=n, shuffle=True, random_state=None, centers = 2, cluster_std = 2.0)
plt.scatter(X[:,0], X[:,1])
```
![0.png]({{ site.baseurl }}/_images/0.png)
After we plug the data into scatter fig, we can see directly that the data are divided into two clusters.Thera
