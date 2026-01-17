# Quantitative Trading System on NIFTY 50

## 📌 Project Overview

This project implements an **end-to-end quantitative trading system for the NIFTY 50 index** using Python.
The system covers the complete workflow from **data collection** to **strategy development**, **regime detection**, and **post-trade analysis**.

The primary objective of this project is to demonstrate how market data, technical indicators, and rule-based logic can be combined into a structured and explainable quantitative trading framework.

---

## 👤 Student Details

* **Name:** Abdul Ghani
* **Roll Number:** 1/22/FET/BCS/108
* **Course:** B.Tech (Computer Science Engineering)
* **Project Type:** Academic / Quantitative Finance Assignment

---

## 📂 Project Structure

```
quant-nifty-strategy/
│
├── DATA/
│   ├── RAW/
│   │   ├── nifty_spot_5min.csv
│   │   ├── nifty_futures_5min.csv
│   │   └── nifty_options_5min.csv
│   │
│   ├── merged/
│   │   ├── nifty_features.csv
│   │   ├── nifty_merged_5min.csv
│   │   └── nifty_with_regime.csv
│
├── NOTEBOOKS/
│   ├── 01_data_fetch.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_regime_detection.ipynb
│   ├── 05_baseline_strategy.ipynb
│   ├── 06_ml_models.ipynb
│   └── 07_outlier_analysis.ipynb
│
├── RESULTS/
│   └── strategy_return_outliers.csv
│
├── PLOTS/
│   └── ├── PLOTS/
│   └── (generated charts and visualizations)

│
├── README.md
└── .gitignore
```

---

## 📊 Data Description

* **Spot Data:** NIFTY 50 5-minute OHLCV data
* **Futures Data:** Synthetic futures derived from spot prices
* **Options Data:** Synthetic options data for feature generation

All datasets are aligned on **5-minute intervals** and merged using timestamps.

---

## ⚙️ Feature Engineering

The following features were engineered:

### Technical Indicators

* EMA (5, 15)
* SMA (20, 50)

### Derivative Market Features

* Put-Call Ratio (PCR)
* Futures Basis
* Implied Volatility (IV)

### Derived Metrics

* Market Returns
* Strategy Returns
* Trend-based features

---

## 📈 Regime Detection

Market regimes were classified into:

* **Uptrend (+1)**
* **Sideways (0)**
* **Downtrend (-1)**

Regimes were determined using:

* Moving average relationships
* Price trend behavior

Regime visualization was plotted over the NIFTY price series.

---

## 💹 Trading Strategy

* **EMA crossover-based strategy**
* Trades filtered using detected market regime
* Long-only / directional trading logic
* Strategy returns computed using position-based returns

---

## 🤖 Machine Learning (Exploratory)

Machine learning models were explored as:

* Signal confirmation tools
* Noise reduction filters

Due to data constraints, ML models were not finalized for deployment, but the framework is included for future extension.

---

## 📉 Performance & Outlier Analysis

Post-trade analysis includes:

* Z-score based outlier detection
* IQR-based outlier detection
* Strategy return distribution analysis

### Visualizations Generated

* Strategy return boxplot
* Strategy returns with highlighted outliers
* Correlation heatmap
* PnL vs trade duration scatter plot
* IV distribution comparison (wins vs losses)

Outlier trades are saved in:

```
RESULTS/strategy_return_outliers.csv
```

---

## 🧠 Key Learnings

* Importance of regime-based filtering in trading strategies
* Feature engineering significantly impacts strategy stability
* Outlier analysis provides deeper insight beyond aggregate returns
* Structured pipelines improve explainability and robustness

---

## 🛠️ Tools & Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* yFinance (for data fetching)

---

## ✅ Conclusion

This project demonstrates a **robust, explainable, and structured quantitative trading workflow** for the NIFTY 50 index.
It integrates data engineering, technical analysis, regime detection, and post-trade evaluation into a single coherent framework suitable for academic and research purposes.

---

## 📎 Notes

* This project is for **educational purposes only**
* Not intended for live trading or financial advice

---

**End of README**
