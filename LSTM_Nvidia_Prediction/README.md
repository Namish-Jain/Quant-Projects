# LSTM Stock Price Prediction: NVIDIA (NVDA)

## Overview
This project implements a **Long Short-Term Memory (LSTM) neural network** to predict NVIDIA (NVDA) stock prices using historical daily data.  
The goal is to explore **deep learning for time series forecasting** in a financial context, combining both **quantitative finance knowledge** and **machine learning techniques**.

---

## Dataset
- Source: Yahoo Finance via `yfinance` Python library  
- Ticker: `NVDA`  
- Date Range: January 1, 2017 – August 27, 2025  
- Data preprocessing:  
  - Min-Max scaling (`0,1`)  
  - Train/test split (80%/20%)  
  - Creation of sliding windows (60 days) for LSTM sequences  

---

## Methodology
1. **Data Collection:** Download historical stock prices using `yfinance`.  
2. **Preprocessing:**  
   - Scale data using `MinMaxScaler`  
   - Create sequences of 60 days of historical prices as input (`X_train`) and the next day as target (`y_train`)  
3. **LSTM Model:**  
   - Sequential Keras model with two LSTM layers, one Dense layer and Dense output  
   - Loss function: Mean Squared Error (MSE)  
   - Optimizer: Adam  
4. **Training:**  
   - Fit model on training sequences  
   - Validate on test data  
5. **Prediction & Evaluation:**  
   - Generate predicted stock prices  
   - Evaluate performance using plots and metrics  

---

## Results
- Comparison of **predicted vs actual stock prices** over the test period  
- Visualization shows how the model captures trends in NVDA prices
- <img width="904" height="446" alt="image" src="https://github.com/user-attachments/assets/59f760d1-1c71-49f4-8fb1-7481be3d45eb" />
- Calculated a root mean squared error of 10.6 (3sf)

---

## Files in this Folder
- `LSTM_NVDA_Prediction.ipynb` → main Colab/Jupyter notebook with code and plots  
- `README.md` → project description

---

## Requirements
```text
Python 3.x
numpy
pandas
matplotlib
yfinance
scikit-learn
tensorflow / keras

