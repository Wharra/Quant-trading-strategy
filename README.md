# 📈 Quant Trading Strategy — Training Project

## 📘 Overview

This project is a **quantitative trading simulation** inspired by a **conference on quantitative finance and algorithmic trading** that I attended.
After the event, I decided to **reproduce and extend** part of the methodology presented — focusing on **stationarity**, **cointegration**, and **z-score–based signal generation** — to better understand how statistical arbitrage strategies are built.

It culminates in a simple **pair trading backtest** between Binance and Deribit BTC futures.

> ⚠️ **Disclaimer**
> This is a **personal training project** created for **educational purposes** only.
> It is **not intended for real trading**, and **no financial results are guaranteed**.
> The goal is to experiment with **Python, econometrics, and quantitative modeling**.

---

## 🧠 Key Concepts

### 1. Stationarity

* Testing time series with the **Augmented Dickey–Fuller (ADF)** test.
* Comparison between stationary and non-stationary simulated data.
* Understanding why stationarity is essential in time-series modeling.

### 2. Cointegration

* Application to two correlated assets (Binance vs. Deribit BTC futures).
* **Engle–Granger two-step method** used to test long-term relationships.
* Interpretation of the residual spread between the two price series.

### 3. Z-Score–Based Signal Generation

* **Z-score** quantifies how far the spread deviates from its mean:
  [
  z = \frac{spread - mean(spread)}{std(spread)}
  ]
* Trading rules:

  * z > +2 → **Enter Short**
  * z < -2 → **Enter Long**
  * |z| < 0.5 → **Exit Position**

### 4. Backtesting

* Simulation of trade entries and exits based on z-score signals.
* Visualization of spread evolution and trading performance over time.

---

## ⚙️ Workflow

1. **Data Collection**

   * Historical BTC futures data fetched using `ccxt` from **Binance** and **Deribit** (15-min intervals).
2. **Data Preprocessing**

   * Computation of spreads and rolling averages for smoothing.
3. **Statistical Analysis**

   * Stationarity and cointegration tests (ADF, Engle–Granger).
4. **Signal Generation & Backtest**

   * Z-score logic applied to create entry/exit signals and visualize the results.

---

## 🧩 Tools & Libraries

* **Python** (Jupyter Notebook)
* **NumPy**, **Pandas**, **Matplotlib**, **Seaborn**
* **statsmodels** (ADF test, OLS regression)
* **ccxt** (market data fetching)

---

## 📊 Outputs

* Comparison of stationary vs. non-stationary simulated series.
* Stationarity and cointegration test results.
* Dynamic plots of spread, z-score, and generated signals.
* Backtest chart showing **entry/exit points** and mean-reversion behavior.

---

## 💼 Learning Goals

* Apply **time series econometrics** to financial markets.
* Understand and test **mean reversion** strategies.
* Learn the practical use of **stationarity and cointegration** in trading.
* Gain experience in **Python-based quantitative finance analysis**.

---

*This notebook was developed as a follow-up to a conference on quantitative trading. It was later extended and adapted for personal learning purposes to better understand financial data modeling and strategy design.*


> “Educational notebook inspired by a quant trading conference — exploring stationarity, cointegration, and mean-reversion strategies.”
