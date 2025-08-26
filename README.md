# 📊 A Quantitative Analysis of U.S. Equities: Forecasting with PCA and Linear Regression  

## 📌 Overview  
This project investigates the use of **Principal Component Analysis (PCA)** and **Linear Regression** to forecast the stock prices of **10 major U.S. equities** between 2015–2025.  
The goal was to analyze the effectiveness of PCA-enhanced regression in predicting stable vs. volatile stocks, and to evaluate portfolio-level performance compared to the **S&P 500 (SPY)**.  

---

## 🛠️ Methodology  
1. **Data Collection**  
   - Daily stock data retrieved from Yahoo Finance (`yfinance`) for 10 equities:  
     `AAPL, MSFT, GOOGL, AMZN, META, NVDA, TSLA, JPM, JNJ, PG`.  

2. **Data Preparation**  
   - Converted prices into **log returns** for stationarity.  
   - Applied **252-day Moving Average (MA252)** to capture long-term trends.  

3. **Dimensionality Reduction**  
   - Applied **PCA** on OHLCV features.  
   - Retained <15 components while preserving over **95% of variance**.  

4. **Forecasting Model**  
   - Linear Regression with rolling **lookback (30 days)** and **forward (30 days)** windows.  
   - Evaluated using **MAE, RMSE, MAPE, R²**.  

---

## 📈 Results  

### 🔹 Prediction Accuracy  
- **Stable Stocks** (PG, JNJ, AAPL, MSFT):  
  - High accuracy, R² > 0.95, low MAE (~\$5–10).  
- **Volatile Stocks** (TSLA, META, NVDA):  
  - Larger forecast errors, struggling with abrupt price swings.  

### 🔹 Portfolio Insights  
- **Equal-weighted portfolio** of all 10 equities:  
  - **Outperformed the S&P 500 (SPY)** in CAGR and Sharpe ratio.  
  - Errors balanced out at portfolio level.  
- **Tech leaders** (NVDA, TSLA) delivered outsized long-term returns.  
- **Defensive stocks** (JNJ, PG) provided stable, low-volatility growth.  

---

## 📊 Key Metrics  
- **Overall MAE:** ≈ \$9  
- **MAPE:** < 8%  
- **R²:** > 0.95 for stable stocks  
- **Portfolio CAGR:** higher than SPY benchmark  

---

## 💡 Takeaways  
- PCA-enhanced regression is an **efficient, interpretable baseline** for forecasting stock trends.  
- Works well for **stable equities**, but volatile stocks require more advanced models (ARIMA, GARCH, LSTMs).  
- Combining growth and defensive stocks in a diversified portfolio leads to better **risk-adjusted performance**.  

---

## ⚙️ Tech Stack  
- **Python Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn, yfinance, statsmodels  
- **Techniques:** Time Series Forecasting, PCA, Regression, Portfolio Evaluation  

---

## 🚀 Future Work  
- Extend to **non-linear models** (ARIMA, GARCH, LSTM).  
- Incorporate **macroeconomic indicators & fundamentals**.  
- Explore **cross-market forecasting** (FX, commodities, bonds).  

---

👤 **Muhammad Umar Amin**  
- 📧 mamin14@lamar.edu
- 🔗 [LinkedIn](https://www.linkedin.com/in/mumaramin-0a6795257/)  
- 📊 [GitHub](https://github.com/Muhammadumaramin)  
