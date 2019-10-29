# Store-Item-Demand-Forecasting-Challenge
This code is used in the Kaggle competition: Store-Item-Demand-Forecasting-Challenge. https://www.kaggle.com/c/demand-forecasting-kernels-only
From this challenge, we can learn how to use machine learning for time series forecasting.
# Getting Started
The code is run in the Colab environment https://colab.research.google.com If you couldn't open the .ipynb file, please paste the link of the file to here: https://nbviewer.jupyter.org/
# Techniques:
Feature Engineering:
1. create several datetime-related features in order to transform the date to several integers, which is more convinient for us to train models.
2. create moving average of sales in order to smooth the noise signal.
3. create the 90-day-before data of shift the sales and its moving average in order to have new features which are not NAN in the test future days.

Model: XGBRegressor

# Outlook:
Use the moving average of sales rather than sales as the target, and then transform the predicted moving average back to the predicted sales. The advantage of using moving average of sales as target:
1. The data is more smooth rather than sales
2. The moving average of sales (with windows=1) doesn't produce any NAN, which occurs in the 90-day-before moving average data.
