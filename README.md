# Stock Market Prediction Using RandomForestClassifier

This project is about predicting the stock market prices using RandomForestClassifier from sklearn. We use the S&P 500 stock market data from Yahoo Finance.

## Data

The data used in this project is obtained from Yahoo Finance using the `yfinance` package. We fetch the historical data of S&P 500 and store it in a CSV file. The data includes the following features:
- Open
- High
- Low
- Close
- Volume

## Project Overview

The project starts by preparing the data for analysis. This involves deleting the 'Dividends' and 'Stock Splits' columns and adding a 'Tomorrow' column which is simply the 'Close' price shifted by one day. We also add a 'Target' column which indicates whether the closing price of the stock increased or decreased on the next day.

We then proceed to train our RandomForestClassifier model on the data, and test it to obtain a precision score. The model is trained and tested multiple times using a backtest strategy.

Furthermore, we also include a few extra features in our model such as rolling averages and trends for various horizons. This improves the precision score of our model.

## Model

The machine learning model used in this project is RandomForestClassifier from sklearn. It is chosen for its ability to handle high dimensional spaces and multicollinearity in an efficient way.

## Results

The model shows a decent precision score and can predict the direction of the S&P 500 index with around 57% accuracy. This is significantly better than random guessing.

