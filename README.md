# Forcasting-AirPassenger
Time Series Forecasting with ARIMA and SARIMA Models

# Overview
This repository contains Python code for time series forecasting using ARIMA (AutoRegressive Integrated Moving Average) and SARIMA (Seasonal AutoRegressive Integrated Moving Average) models. The code takes a dataset of monthly airline passenger numbers as an example and demonstrates the steps involved in building and evaluating these models for time series forecasting.

# Prerequisites
1, Python 3.x
2. Jupyter Notebook (optional, for running the provided code notebooks)
3.Required Python libraries: pandas, matplotlib, statsmodels, pmdarima, numpy

# Data
The dataset used for this project is the "AirPassengers" dataset, which contains monthly airline passenger numbers from a specific time period. You can find this dataset in the repository under data/AirPassengers.csv. Ensure that you have this dataset or replace it with your own time series data.

# ARIMA Model
The ARIMA model is built and evaluated in the following steps:

1. Stationarity Check: The stationarity of the time series data is checked using the Augmented Dickey-Fuller (ADF) test. The null hypothesis (H0) is that the data is non-stationary, and the alternative hypothesis (H1) is that the data is stationary. The significance level is set at 0.05.

2. Differencing: If the data is found to be non-stationary, differencing is applied to make it stationary. The differencing process and its effects on the data are visualized.

3. ACF & PACF Plots: Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) plots are created to determine the values of p, d, and q for the ARIMA model.

4. Auto ARIMA Model Selection: The pmdarima library is used to automatically select the optimal p, d, and q values for the ARIMA model using the ADF test.

5. Model Fitting and Forecasting: The ARIMA model is fitted to the data, and in-sample and out-of-sample forecasts are generated.

6. Accuracy Metrics: The Mean Absolute Percentage Error (MAPE) is calculated to assess the accuracy of the ARIMA model's forecasts.

# SARIMA Model
The SARIMA model follows a similar process to the ARIMA model, but it also considers seasonality:

1. Seasonal Stationarity Check: The stationarity of the seasonally differenced time series data is checked using the ADF test.

2. Seasonal Differencing: If the seasonally differenced data is found to be non-stationary, seasonal differencing is applied.

3. ACF & PACF Plots: ACF and PACF plots are created for the seasonally differenced data to determine the values of p, d, and q for the seasonal part of the SARIMA model.

4. Auto SARIMA Model Selection: The pmdarima library is used to automatically select the optimal p, d, P, D, and Q values for the SARIMA model.

5. Model Fitting and Forecasting: The SARIMA model is fitted to the data, and in-sample and out-of-sample forecasts are generated, including seasonality.

6. Accuracy Metrics: The MAPE is calculated to assess the accuracy of the SARIMA model's forecasts.

# Usage
1. Clone the repository: git clone https://github.com/your-username/time-series-forecasting.git
2. Set up your Python environment and install the required libraries.
3. Run the Jupyter notebooks or Python scripts to experiment with ARIMA and SARIMA models on your own time series data.
   
# Contributions
Contributions, bug reports, and feedback are welcome! Feel free to open issues or submit pull requests to improve this project.
