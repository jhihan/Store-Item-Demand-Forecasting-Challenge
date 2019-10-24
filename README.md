# Store-Item-Demand-Forecasting-Challenge
This code is used in the Kaggle competition: Store-Item-Demand-Forecasting-Challenge. https://www.kaggle.com/c/demand-forecasting-kernels-only
From this challenge, we can learn how to use machine learning for time series forecasting.
# Getting Started
The code is run in the Colab environment https://colab.research.google.com If you couldn't open the .ipynb file, please paste the link of the file to here: https://nbviewer.jupyter.org/
# Techniques:
Feature Engineering:
1. create several datetime-related features in order to transform the date to several integers, which is more convinient for us to train models.
2. shift the sale price so that the the “lagged” sale values can be used to predict the future price. Because we will predict 90-days data, we choose the sale price 90 days ago as a new feature for training.

Model: XGBRegressor
