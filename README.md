![Python 3.5](https://img.shields.io/badge/python-3.5-blue.svg)

# Wine-Quality
Coursework from [Harvard CS 109](http://nbviewer.jupyter.org/github/cs109/2014/blob/master/homework/HW5.ipynb)

Predict wine quality based on the chemical properties of the wine.

## Data
### Data Source
Wine quality dataset from [UCI website](https://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/)

Focus on the red wine only.

### Data Preview
**11 chemical properties**, including the concentration of sugar, citric acid, alcohol, pH etc.

The **wine qualities** are represented as integers scaling from **1 to 10**.
<p align="justify">
   <img src="https://github.com/xuwenyihust/Wine-Quality/blob/master/graphs/head.JPG" width="900"/>
</p>
```python
>>> print(wine.shape)
(1599, 12)
```

## Process

* Data Wrangling
    * Pick out the **feature matrix X & response vector y**, transform them into Numpy arrays
    * Convert 0~10 ratings to good(1)/bad(0) **binary classifications** (Threshold = 7)

* Model Construction 
    * Choose **random forests** method to do the classification

## Libraries Used
* [pandas](http://pandas.pydata.org/)
* [matplotlib](http://matplotlib.org/)
* [sklearn](http://scikit-learn.org/stable/)
* [numpy](http://www.numpy.org/)
* [seaborn](https://stanford.edu/~mwaskom/software/seaborn/)

## Appendix
### How to construct a random forest
> **Construct a multitude of decision trees** at training time and output the class that is the mode of the classes (classification) or mean prediction (regression) of the individual trees.

### Advantages of random forests over decision trees
> Random decision forests correct for decision trees' habit of overfitting to their training set.

## Resources
[Harvard CS 109 HW5](http://nbviewer.jupyter.org/github/cs109/2014/blob/master/homework/HW5.ipynb)
[UCI wine-quality dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/)
[Wikipedia Random Forests](https://en.wikipedia.org/wiki/Random_forest)
[Hastie, Trevor; Tibshirani, Robert; Friedman, Jerome (2008). The Elements of Statistical Learning (2nd ed.). Springer. ISBN 0-387-95284-5.](http://statweb.stanford.edu/~tibs/ElemStatLearn/)
