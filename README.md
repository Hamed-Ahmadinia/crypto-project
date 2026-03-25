# Cryptocurrency Time-Series Forecasting Project

## Overview

This project develops an end-to-end pipeline for **cryptocurrency time-series analysis and forecasting** using high-frequency market data. The workflow integrates **data acquisition, preprocessing, feature engineering, and deep learning modeling**, focusing on reproducibility and scalability.

---

## System Architecture

```mermaid
flowchart LR
    A[Binance API] --> B[Raw Data Collection]
    B --> C[Data Preprocessing]
    C --> D[Feature Engineering]
    D --> E[LSTM Model Training]
    E --> F[Predictions]
    F --> G[Evaluation & Results]
```

---

## Data Pipeline

```mermaid
flowchart TD
    A[API Request] --> B[Download OHLCV Data]
    B --> C[Store as Parquet Files]
    C --> D[Load into DataFrame]
    D --> E[Clean & Sort Data]
    E --> F[Ready for Feature Engineering]
```

---

## Feature Engineering Process

```mermaid
flowchart LR
    A[Close Price] --> B[Returns]
    A --> C[Log Returns]
    A --> D[Rolling Mean]
    A --> E[Rolling Std]
    B --> F[Feature Set]
    C --> F
    D --> F
    E --> F
```

---

## Model Workflow (LSTM)

```mermaid
flowchart TD
    A[Time Series Data] --> B[Sliding Window Creation]
    B --> C[Input Sequences]
    C --> D[LSTM Network]
    D --> E[Predicted Price]
```

---

## Data Collection

* Source: Binance API
* Assets: BTC, ETH, ADA, etc.
* Time Range: 2021 – Present
* Frequency: configurable (1m, 15m, etc.)

Dataset scale:

* ~500K rows per coin (15m)
* Millions of rows (1m)

---

## Project Structure

```text
crypto_project/
│
├── crypto_api_lstm_puhti_Ahmadinia.ipynb   # Main notebook
├── data/                                   # Raw data (excluded)
├── models/                                 # Trained models (excluded)
├── checkpoints/                            # Training checkpoints (excluded)
├── results/                                # Outputs (excluded)
├── logs/                                   # Logs (excluded)
└── .gitignore
```

---

## Computational Environment

* Platform: **CSC Puhti (HPC)**
* Parallel processing for large datasets
* Long-running training jobs (~hours)

---

## Reproducibility

To reproduce:

1. Set parameters:

   * `START_DATE`
   * `INTERVAL`
   * `SYMBOLS`
2. Run notebook sequentially
3. Data will be downloaded automatically via API

---

## Limitations

* High computational cost for 1-minute data
* Long data preparation time (~hours)
* Market volatility and noise

---

## Future Work

* Transformer models (attention-based)
* Hyperparameter tuning
* Multi-asset modeling
* Real-time prediction system

---

## Author

**Hamed Ahmadinia**

Data Analytics & Machine Learning

---

## Notes

Raw datasets, models, and intermediate outputs are excluded from GitHub due to size and reproducibility considerations.
