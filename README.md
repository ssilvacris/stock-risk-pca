# Stock Risk Profiling using PCA and Clustering

Project combining **Finance** and **Data Science** to segment stocks by their risk–return profiles using **PCA (Principal Component Analysis)** and **Clustering**.

---

## 🎯 Objective
Group stocks according to risk and performance metrics (mean return, volatility, drawdown, etc.) using **PCA** to reduce dimensionality and **K-Means** (optionally hierarchical clustering) for segmentation.

---

## 🧠 Methodology
1. **Data collection** via `yfinance` (adjusted daily prices).  
2. **Feature engineering** for risk and return metrics:  
   - Mean daily and annualized return  
   - Daily and annualized volatility (standard deviation)  
   - Maximum drawdown  
   - Downside deviation  
   - Sharpe ratio (rf ≈ 0% for simplicity, adjustable)  
   - *Optional:* Beta vs. market index  
3. **Standardization** of variables (z-score).  
4. **PCA** for compressing correlated variables and analyzing explained variance.  
5. **Clustering** (K-Means) with *k* selection based on **silhouette score**; comparison with hierarchical clustering.  
6. **2D visualization** (PC1 × PC2) with color-coded clusters.  
7. **Export** of tables containing PCA scores, cluster labels, and metrics.

---

## 📊 Data
- **Source:** Yahoo Finance via `yfinance`.  
- Supports stocks from **B3** (Brazil, suffix `.SA`) or **European/American** markets.  
- The notebook includes an editable list of stock tickers.

---

## 🗂️ Project Structure
```
stock-risk-profiling/
├── data/                  # raw and processed datasets
├── notebooks/             # Jupyter notebooks with analyses
├── src/                   # reusable Python scripts
├── results/               # figures, tables, final outputs
├── requirements.txt       # dependencies
└── README.md              # this file
```

---


[See the notebook here](stock-risk-profiling/notebooks)



---

## ⚖️ License
MIT License — free to use, modify, and share with proper attribution.  
Includes no warranty.

---

*Last updated: 2025-10-07*
