# Boston House Prices Analysis/Neural Network Project

## This is a Jupyter notebook that analyses the Boston Housing dataset.

It compares the median house prices with regard to whether or not they are near or far from the Charles River (CHAS), it also compares the median house price to the number of rooms (RM). It plots the data using scatterplots and bar charts, and runs some descriptive statistics to find the mean, max, median, standard deviation and variance of the feature set. 

It also uses inferential statistics on the dataset, running regression analyses, and Student's TTest and ANOVA tests to find any differences in the means of the data for the MEDV (median value) and CHAS (proximity to river) variables. The variables are also explored using line plots and a boxplot to understand more about the data. 

It then uses the Keras Neural Network to make accurate predictions about the output variable (MEDV), using CHAS, zoning (ZN), pupil teacher ratio (PTRATIO), low socioeconomic status (LSTAT) as the input variables.



## How to use this notebook

you can clone the repository to your local machine using:

```shell
git clone 
```

To run the notebook, you must first install Jupyter Notebooks. It is recommended that you install the package manager Anaconda, which comes bundled with Python 3 and Jupyter.
The guide to installing Anaconda is [here](https://docs.anaconda.com/anaconda/install/).
A guide is [here](https://jupyter.readthedocs.io/en/latest/install.html).

To run the notebook, open a terminal or bash window and type:
```bash
jupyter notebook
```
This will automatically open the Jupyter file directory GUI in your browser at localhost:8888. From here you can open the boston-house-prices-analysis.ipynb file.
When the notebook opens, click on cell > run all to run all cells.




