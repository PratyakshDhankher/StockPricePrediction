# StockPricePrediction
This project leverages Long Short-Term Memory (LSTM) neural networks to predict stock prices using historical data. The model delivers exceptional accuracy and demonstrates practical applicability to Indian stock market predictions.

## 📊 Project Summary

Metric	Value

Dataset Size	5306 samples

Features Used	6 numerical columns

Training Epochs	50

R² Score	0.9975

MAPE	0.87%

MAE	₹3.32

2% Tolerance Accuracy	92.47%

Directional Accuracy	79.83%

## 📁 Dataset Info
Stock Symbol: ICICIBANK (You can choose the stock of your choice)

Time Range: 2000 – 30-04-2021

Source: Kaggle NSE Stock Dataset

Size: 5306 rows × 15 columns

Price Range: ₹67.40 – ₹1794.10

Used Features: ['Open', 'High', 'Low', 'Last', 'VWAP', 'Volume']

## Sample Rows

| Date       | Symbol    | Open  | High  | Low   | Close |
|------------|-----------|-------|-------|-------|-------|
| 2000-01-03 | ICICIBANK | 74.35 | 74.75 | 71.40 | 74.75 |
| 2000-01-04 | ICICIBANK | 73.05 | 78.50 | 71.00 | 73.05 |



## 🏗️ LSTM Model Architecture
Model: "sequential"

| Layer (Type)   | Output Shape | Parameters |
|----------------|--------------|------------|
| LSTM           | (None, 1, 50) | 11,400     |
| LSTM           | (None, 50)    | 20,200     |
| Dense          | (None, 1)     | 51         |
| **Total**      | —             | **31,651** |


Total params: 31,651
Trainable params: 31,651

## 🎯 Evaluation Metrics (ICICI BANK)
R² Score: 0.9975

MAPE: 0.87%

MAE: ₹3.32

Within 1% Tolerance: 69.30%

Within 2% Tolerance: 92.47%

Within 5% Tolerance: 99.44%

Directional Accuracy: 79.83%

#📋 Sample Predictions
| Sample | Actual (₹) | Predicted (₹) | Error (%) | Error (₹) |
|--------|------------|---------------|-----------|-----------|
| 1      | 268.05     | 268.08        | 0.01%     | 0.03      |
| 2      | 269.30     | 268.53        | 0.29%     | 0.77      |
| 3      | 268.40     | 269.07        | 0.25%     | 0.67      |


## 📌 Project Features

✅ Handles real-world stock data with missing values

📐 Scales and reshapes data for LSTM input

📊 Uses multiple evaluation metrics: R², MAPE, MAE, and directional accuracy

📉 Plots losses and provides tolerance-based error metrics

🇮🇳 Adapted to INR and Indian stock market data
