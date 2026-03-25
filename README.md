# Cryptocurrency Time-Series Forecasting Project

## Overview

This project develops an end-to-end pipeline for **cryptocurrency time-series analysis and forecasting** using high-frequency market data. The workflow integrates **data acquisition via API, preprocessing, feature engineering, and deep learning modeling**, with a focus on scalable and reproducible experimentation.

The primary objective is to model and predict short-term price dynamics using advanced sequence models such as **Long Short-Term Memory (LSTM)** networks.

---

## Data Collection

Market data is collected programmatically from the **Binance API**, covering multiple major cryptocurrency pairs (e.g., BTCUSDT, ETHUSDT, ADAUSDT).

* Time range: January 2021 – Present
* Frequency: configurable (e.g., 1-minute, 15-minute intervals)
* Data type: OHLCV (Open, High, Low, Close, Volume)

Due to the high resolution and extended time horizon, the dataset reaches **millions of observations per asset**, resulting in large storage requirements.

---

## Feature Engineering

The project includes systematic feature construction to capture market dynamics:

* Returns and log-returns
* Rolling statistics (mean, standard deviation)
* Volatility indicators
* Window-based transformations

These features are designed to enhance temporal pattern recognition and improve model performance.

---

## Modeling Approach

The core modeling framework is based on **deep learning architectures for sequential data**, including:

* LSTM (Long Short-Term Memory) networks
* Sliding window sequence generation
* Supervised learning formulation of time-series forecasting

The models are trained on historical sequences to predict future price movements.

---

## Project Structure

```
crypto_project/
│
├── crypto_api_lstm_puhti_Ahmadinia.ipynb   # Main notebook
├── data/                                   # Raw and processed datasets (excluded from GitHub)
├── models/                                 # Trained models (excluded)
├── checkpoints/                            # Training checkpoints (excluded)
├── results/                                # Outputs and predictions (excluded)
├── logs/                                   # Execution logs (excluded)
└── .gitignore
```

---

## Computational Environment

This project was developed and executed on **CSC Puhti (HPC environment)**, enabling efficient handling of large-scale time-series data and extended training procedures.

---

## Reproducibility

To reproduce the results:

1. Configure API access for Binance data
2. Adjust parameters such as:

   * `START_DATE`
   * `INTERVAL`
   * selected trading pairs
3. Execute the notebook sequentially

Note: Raw datasets and model artifacts are excluded from the repository due to size constraints.

---

## Limitations

* High-frequency data significantly increases computational cost
* Long training times (several hours for full datasets)
* Market noise and non-stationarity remain inherent challenges

---

## Future Work

* Integration of Transformer-based architectures
* Hyperparameter optimization
* Multi-asset correlation modeling
* Deployment for real-time prediction

---

## Author

**Hamed Ahmadinia**

Specialization: Data Analytics & Machine Learning

---

## License

This project is intended for academic and research purposes.
