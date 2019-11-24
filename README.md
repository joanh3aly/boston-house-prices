# Boston House Prices Analysis/Neural Network Project

[[_TOC_]]

## This is a Jupyter notebook that analyses the Boston Housing dataset.

It compares the median values of housing with regard to whether or not they are near or far from the Charles River (CHAS). It runs some descriptive to find the mean, max, median, standard deviation and variance . 

The variables are explored using line plots and boxplot to understand more about the data. It also uses inferential statistics on the dataset, running Student's TTest and ANOVA to find any differenes in the means of the data. 

It then uses the Keras Neural Network to (try to) make accurate predictions about the target variable, using the CHAS as the target variable.



## How to use this notebook

you can clone the repository to your local machine using:

```shell
git clone 
```

To run the notebook, you must first install Jupyter Notebooks. It is recommended that you install the package manager Anaconda, which comes bundled with Python 3 and Jupyter.
The guide to installing Anaconda is (here)[https://docs.anaconda.com/anaconda/install/].
A guide is (here)[https://jupyter.readthedocs.io/en/latest/install.html].

To run the notebook, open a terminal or bash window and type:
```bash
jupyter notebook
```
This will automatically open the Jupyter file directory GUI in your browser at localhost:8888. From here you can open the boston-house-prices-analysis.ipynb file.
When the notebook opens, click on cell > run all to run all cells.

..

Initial plan - 

1/ Describe (**Good summary of the dataset, repository well laid-out and organised. Reasonable commits to the repository**):
- <s>Download/import dataset</s>
- Run basic exporatory analysis of dataset - df.head, find mean, max, min, median, variance etc - esp wrt housing near the charles river as the main feature for analysis.
- Plot the data using matplotlib/seaborn (https://nbviewer.jupyter.org/github/ianmcloughlin/jupyter-teaching-notebooks/blob/master/simple-linear-regression.ipynb)
- Find the slope and cost
- Find the line of best fit

OBSERVATIONS:
The values of MEDV are distributed normally with few outliers.
RM has a strong positive correlation with MEDV (0.7) where as LSTAT has a high negative correlation with MEDV(-0.74).
0.18 indicates a positive correlation of CHAS with MEDV, although it is not particularly strong.



2/ Infer (**Appropriate analysis of the relationship between the median house price and whether the house borders the river, with good explanations of the analysis**)
- Investigate locations of houses, find patterns.
- Find median (analyse whether there is a significant difference in median house prices between houses that are along the Charles river and those that aren’t)

OBSERVATIONS:
0.18 indicates a positive correlation with MEDV, although it is not particularly strong.
CHAS is binary, therefore there are only 2 x values (1 or 0). The spread of MEDV is from 0 to 50, when the house is far from the river. The spread of MEDV is mostly from 12 to 35 when the house is near the river, or so it appears.
As the data is not linear, we will not get a linear distribution as is the case for the RM feature variable. Is there any point in getting the slope?
A boxplot might be more relevant? There is no point in doing regression analysis, as MEDV is a classifier?

Boxplot:
The 50th percentile of the data is almost the same in both plots (~21 and 23 respectively). However, it appears that the majority of the data for the houses near the river are in the 75th percentile. The minimum value is 14 thousand and the max value is 50 thousand. The values for these houses are significantly higher than houses away from the river, as 50% of the data are between 21 and 33 thousand. It appears that the houses far from the river are significantly cheaper, with 50% of the data spread between 17 and 25 thousand. The min value is 3 and the max is 37, if you don't include the outliers. There are many outliers at the high end of the spectrum however, representing houses that are very expensive, yet far from the river.

TTest:
Ttest_indResult(statistic=-3.996437466090509, pvalue=7.390623170519905e-05)
Very small probability that they are the same? Probability is < 0.05, at 0.00000739, therefore the average median house price for the riverside properties is different to the average median house price for the properties far from the river.
We can see that there are only 35 houses near the river, yet there are 471 houses far from the river. Does this disparity have an effect on the calculated outcome? (In ANOVA it matters that the sample sizes to be compared are similar.)




3/ Predict (**Well-trained neural network providing decent predictions of house prices based on the other variables. Good explanations of how to use the neural network and how it works**)
- Use keras [7] to create a neural network that can predict the median house price based on the other variables in the dataset.
- ??

Tried some NN testing:
Predictions for near/far to charles river is not very accurate (logical errors in code?).
Other predictions might be LSTAT or CRIM might be some other variables to test along with CHAS.


