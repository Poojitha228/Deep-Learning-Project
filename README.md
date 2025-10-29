# Deep-Learning-Project
Stock market trend prediction by using LSTM sequence model with 94% accuracy

##Project Overview

This project predicts stock market trends using historical data and a deep learning LSTM model.
It classifies the next 5 candles as Uptrend, Downtrend, or Neutral by analyzing previous time steps.

##Objective

To build a predictive model that determines stock movement direction for the next 5 intervals using past stock indicators.

##Dataset
File: large_32.csv
Features: Date Time, Open, High, Low, Close, Volume, SMA 5, SMA 10, SMA 50, RSI 14, MACD Line, MACD Signal, MACD Histogram, Bollinger Bands, Alligator Indicators, EMA 9, KAMA, ATR, RMA 14, Smooth MA 14, WMA 14.

##Label Generation
Uptrend – All 5 upcoming candles have Close > Open
Downtrend – All 5 upcoming candles have Close < Open
Neutral – Mixed green and red candles

##Steps
Data loading and cleaning in Google Colab
Feature selection and label creation
Time sequence generation of 20 candles
Data splitting and normalization
LSTM model building and training
Evaluation using accuracy and loss metrics
Model saved as stock_model.keras

##Results
Training Accuracy: 94.3%
Validation Accuracy: 94.1%
Validation Loss: 0.26
The model achieved stable convergence without overfitting.

##How to Run
Open the notebook in Google Colab
Mount Google Drive
Upload large_32.csv
Update the file path and run all cells
Model will be saved automatically in your Drive

##Dependencies
pandas, numpy, tensorflow, scikit-learn, matplotlib

#Install with:
pip install pandas numpy tensorflow scikit-learn matplotlib

##Insights and Challenges
Handled missing values, tuned window size and sequence order to prevent data leakage, and found LSTM more effective than traditional models.

##Future Enhancements
Add GRU or Transformer models, include sentiment analysis, and deploy as a web app using Flask or Streamlit.

##Author
Poojitha Boinasetty
Email: boinasettypoojitha@gmail.com
GitHub: https://github.com/Poojitha228
LinkedIn: https://www.linkedin.com/in/poojitha-boinasetty
