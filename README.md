# Tabular Data: Deep Learning vs Random Forest

This model compares the results of using a deep learning algorithm vs using a random forest algorithm for tabular data. The deep learning model was built using PyTorch and the fastai library. The data comes from a Kaggle competition called [House Prices](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data). The goal is to predict the price of a house given the characteristics in the dataset.

The metric used for the error was the root mean squared percentage error (RMSPE).

<img src="https://github.com/mlsmall/Deep-Learning-vs-Random-Forest/blob/master/RMSPE.png" width="300" />

where yi denotes the sales price for a house and yhati denotes its corresponding prediction. 

The random forest regressor achieved a better RMSPE score of 12.4%, while the deep learning model achieved a score of 17.4%.

## Deep Learning Model
The model is built using PyTorch and the fastai library. 

### Preprocessing
- Filled missing values for numerical variables with the median of the column.
- Categorical variables were turned into Pandas categories. Then each categorical variable was assigned a numerical code.
- Continuous variables were normalized using the mean and the standard deviation.

### Network Acrhitecture
- An intermediate weight matrix of 200 activation inputs to 100 activation outputs
- Batch normalization was applied to every continues variable
- 2 hidden layers: linear-relu-batch norm, linear-relu-batch-norm

### Training
- 50 epochs
- Training time: 37 seconds
- learning rate: 1e-2
- weight decay: 0.1

## Random Forest Regression

### Preprocessing
- Filled missing values for numerical variables with the median of the column.
- Categorical variables were turned into Pandas categories. Then each categorical variable was assigned a numerical code.
- No normalization on continuous variables

### Acrhitecture
- Forest with 200 trees


### Other Metrics
- R2 Score: 0.914
- RMSE: $23,510
