# Time-Series-Modelling-Case-Study-
German Electricity Load Forecasting
Project Overview

This project forecasts German electricity demand using hourly load data from January 2015 to September 2020. It compares simple benchmarks, statistical models, machine-learning regression and deep learning to determine whether advanced methods can outperform a strong Seasonal Naive forecast.

Data

The analysis uses German electricity load observations from the Open Power System Data platform. Hourly demand is aggregated into daily and weekly averages.

Berlin temperature data is included as an external variable for conditional forecasting.

Analysis

The workflow includes:

Data cleaning and chronological splitting
Hourly, daily and weekly aggregation
Exploratory data analysis
Seasonal decomposition
ADF stationarity testing
ACF and PACF analysis
First and seasonal differencing
Two-year forecasting
Model comparison and residual analysis
Models

The following forecasting methods are evaluated:

Mean forecast
Naive forecast
Seasonal Naive forecast
Drift forecast
SARIMA
SARIMAX with temperature
Gradient Boosting Regressor
LSTM neural network
Evaluation

Forecasts are compared using:

Root Mean Squared Error
Mean Absolute Error
Symmetric Mean Absolute Percentage Error
Improvement relative to Seasonal Naive

Seasonal Naive is used as the main benchmark because German electricity demand shows strong annual seasonality.

Main Findings

Seasonal Naive was the strongest simple benchmark and outperformed Mean, Naive and Drift forecasts.

Gradient Boosting produced competitive weekly forecasts but did not improve on Seasonal Naive. The LSTM produced the lowest numerical error after hourly forecasts were aggregated into weekly averages. However, the LSTM represents a rolling short-term forecasting approach rather than a single fixed two-year forecast.

The SARIMA and SARIMAX outputs require further correction because their forecasts were produced on an incorrect scale following differencing.

Requirements
Python 3
pandas
NumPy
Matplotlib
scikit-learn
statsmodels
TensorFlow
requests
Running the Analysis
Open the notebook in Google Colab or Jupyter Notebook.
Install the required libraries.
Run all cells in order.
Allow the SARIMA parameter search and LSTM training to complete.
Review the generated plots and evaluation tables.
Outputs

The analysis produces:

Load and seasonal decomposition plots
Stationarity and autocorrelation results
Benchmark forecast comparisons
SARIMA residual diagnostics
Gradient Boosting forecasts
LSTM training and forecast plots
Final model evaluation tables
Future Improvements

Future work should correct the SARIMA forecast scale, add detailed German holiday variables, use forecasted rather than observed future temperature, and compare rolling LSTM predictions with a fully recursive long-term forecast.
