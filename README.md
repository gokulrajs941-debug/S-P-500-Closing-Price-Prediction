# S-P-500-Closing-Price-Prediction
S&amp;P 500 closing price prediction using LSTM neural networks, comparing price-level and return-based forecasting approaches.

# S&P 500 Closing Price Prediction Using LSTM Neural Networks

## Project Overview

This project investigates whether Long Short-Term Memory (LSTM) neural
networks can predict the next-day closing price of the S&P 500 index.

The project compares two approaches:

- Absolute closing price prediction
- Daily percentage return prediction

Both models are compared against a naive persistence baseline.

## Dataset

Historical daily S&P 500 data was obtained using the `yfinance` Python
library.

The dataset contains:

- Open
- High
- Low
- Close
- Volume

Additional technical indicators were created:

- 10-day Moving Average (MA10)
- 50-day Moving Average (MA50)
- 14-day Relative Strength Index (RSI)

## Methodology

The data was scaled using Min-Max normalisation and converted into
60-day sequences.

The data was split chronologically:

- 80% training
- 20% testing

The LSTM architecture consists of:

- LSTM layer: 64 units
- LSTM layer: 32 units
- Dense layer: 16 units
- Output layer: 1 unit

## Results

The price-level LSTM achieved:

- RMSE: 221.32 points
- MAE: 196.09 points
- MAPE: 2.72%
- Directional Accuracy: 48%

The naive baseline performed substantially better:

- RMSE: 58.50 points
- MAE: 44.69 points
- MAPE: 0.64%

The return-based LSTM achieved:

- MAE: 0.00676
- RMSE: 0.00871
- Directional Accuracy: 45.41%

## Conclusion

Neither LSTM model outperformed the naive persistence baseline.
The return-based model also showed near-constant predictions,
indicating mode collapse.

The project demonstrates the difficulty of predicting short-term
S&P 500 movements using historical price and volume information alone.

## Technologies

- Python
- TensorFlow / Keras
- Scikit-learn
- Pandas
- NumPy
- yfinance
- Matplotlib

## Author

Gokul Raj Srinivasan
