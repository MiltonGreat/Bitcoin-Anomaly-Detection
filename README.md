# Bitcoin Anomaly Detection using Autoencoder

![screenshot-localhost_8888-2025 03 30-12_59_04](https://github.com/user-attachments/assets/40082584-8baf-47e7-8cdc-684bba252e8d)

## Overview

This project applies deep learning techniques to detect anomalous price movements in Bitcoin's historical data. We developed an autoencoder-based anomaly detection system that learns normal price behavior and identifies unusual price fluctuations. This method helps to uncover significant market events, price manipulations, and potential trading opportunities.

### Dataset

The dataset contains Bitcoin price data at 1-minute intervals (high-frequency data). The columns include:

- **Timestamp:** Unix timestamp (epoch time).
- **Open:** The price at the start of the minute.
- **High:** The highest price reached during the minute.
- **Low:** The lowest price reached during the minute.
- **Close:** The final price at the end of the minute.
- **Volume:** The number of Bitcoins traded during that minute.
- **datetime:** A converted, human-readable timestamp.

The dataset starts at January 1, 2012 and contains data points up to at least January 3, 2012.

### Methodology

1. Data Preprocessing
- Cleaned and normalized price, return, and volatility data.
- Split the dataset into training and testing sets.

2. Autoencoder Model
- Built a deep learning autoencoder using TensorFlow/Keras.
- Trained it to reconstruct normal price behavior.
- Used Mean Squared Error (MSE) as the loss function.

3. Anomaly Detection
- Computed reconstruction errors for each data point.
- Set a threshold for anomalies based on error distribution.
- Flagged high-error points as anomalies.

### Results

The model successfully detected historical Bitcoin anomalies, including:

- April 2013: Early extreme price swings.
- December 2017: Bitcoin’s all-time high near $20,000.
- March 2020: Market crash due to COVID-19.
- June 2022: Crypto market downturn.

The highest anomalies corresponded to high volatility events, confirming the model's effectiveness.

### Future Improvements

1. Optimize threshold selection for better anomaly precision.
2. Use additional features like trading volume & social sentiment for better accuracy.

### Source

![Bitcoin Historical Data from Kaggle](https://www.kaggle.com/datasets/mczielinski/bitcoin-historical-data)
