# 📈 Predictive Market Sentiment Engine (Time Series Analysis)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?logo=pandas)](https://pandas.pydata.org/)
[![Statsmodels](https://img.shields.io/badge/Statsmodels-Time_Series-orange.svg)](https://www.statsmodels.org/)
[![yfinance](https://img.hash.com/badge/Data-yfinance-green.svg)]()

> **Note:** This project is the advanced predictive continuation of my previous foundational research: [Market Sentiment Risk Analysis](https://github.com/Amber-s-art/Market-Sentiment-Risk-Analysis).

## 🚀 Overview
Financial markets are driven by an unobservable, latent variable: **Market Sentiment**. While my previous project focused on extracting this sentiment, this repository acts as an **Advanced Forecasting Engine**. 

By processing 15 years of daily market data across 15 high-influence macroeconomic proxies and blue-chip equities, this project mathematically constructs a single "Fear/Greed" index via **Principal Component Analysis (PCA)**. I then deploy rigorous statistical testing and time-series modeling (**ARIMA & GARCH**) to forecast not just the *direction* of the market, but the impending *volatility risk*.

## 🧠 The Architecture Pipeline

1. **Automated Data Ingestion:** Engineered a robust data pipeline utilizing `yfinance` to scrape, merge, and clean 15 years of daily OHLCV data for global indices (Nifty50, S&P500), commodities (Gold, Brent Crude), currencies (USD/INR), and heavy-weight Indian equities.
2. **Feature Engineering:** Calculated daily logarithmic returns and rolling volatility to normalize disparate asset classes into comparable financial metrics.
3. **Dimensionality Reduction (PCA):** Synthesized 30 complex financial variables down to their First Principal Component (PC1), successfully isolating the underlying "Latent Sentiment Index."
4. **Statistical Validation:** Conducted Augmented Dickey-Fuller (ADF) tests proving stationarity, and Variance Ratio tests confirming the presence of market momentum (rejecting the Random Walk hypothesis).
5. **Predictive Modeling:** * Deployed an **ARIMA(5,0,1)** model to accurately forecast the 30-day directional trend of market sentiment.
   * Engineered a **GARCH(1,1)** model to capture "volatility clustering," effectively quantifying short-term market turbulence and risk.

## 📊 Key Insights for Stakeholders
* **The Market Has Memory:** Statistical testing definitively rejected the Random Walk hypothesis. Our Latent Sentiment Index exhibits strong momentum—positive days mathematically increase the probability of subsequent positive days.
* **Volatility Clusters are Predictable:** The GARCH modeling successfully captured the "ARCH effect," proving that periods of market panic cluster together, allowing us to forecast the "turbulence" of the upcoming 30 days, not just the price target.
* **Heavyweight Influence:** The PCA Loadings Matrix revealed that banking sector heavyweights (like HDFC and ICICI) act as the primary anchors for broader market sentiment, outweighing global macroeconomic proxies in the Indian context.

## 🛠️ Tech Stack & Methodologies
* **Languages & Libraries:** Python (Pandas, NumPy, Matplotlib, Seaborn)
* **Data Engineering:** `yfinance`, Time-Series Forward/Backward Imputation
* **Statistical Modeling:** `statsmodels`, `arch` (ARIMA, GARCH, ADF Testing, Variance Ratio Testing)
* **Machine Learning:** `scikit-learn` (Principal Component Analysis)

## 💻 Local Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YourUsername/Predictive-Market-Sentiment-Engine.git](https://github.com/YourUsername/Predictive-Market-Sentiment-Engine.git)
   cd Predictive-Market-Sentiment-Engine
