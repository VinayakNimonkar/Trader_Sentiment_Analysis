# Trader Performance vs Market Sentiment

## 📌 Objective
This project analyzes how Bitcoin market sentiment (Fear vs Greed) influences trader behavior and performance on Hyperliquid.  
The goal is to identify behavioral patterns and propose actionable trading strategy insights.

---
## Project Folder Struture - Trader-Sentiment-Analysis/
│
├── data/
│   ├── fear_greed.csv
│   └── hyperliquid_trades(1).csv
│
├── notebooks/
│   └── analysis.ipynb
    └── Summary.txt
│
├── requirements.txt
└── README.md


## 📂 Datasets Used

### 1️⃣ Bitcoin Market Sentiment
- Columns: Date, Classification (Fear / Greed)
- Daily sentiment classification

### 2️⃣ Historical Trader Data (Hyperliquid)
- Fields: account, symbol, execution price, size, side, time, closedPnL, leverage, etc.
- Trade-level dataset

---

## 🧹 Data Preparation

### ✔ Initial Checks
- Verified number of rows and columns
- Checked missing values and duplicates
- Converted timestamps to datetime format
- Aligned both datasets at daily level

### ✔ Data Merge
Trader data was merged with sentiment data on the date column to analyze performance under different sentiment regimes.

---

## ⚙️ Feature Engineering

The following key metrics were created:

- Daily PnL per account
- Win rate per trader
- Average trade size
- Leverage distribution
- Trade frequency per day
- Long/Short ratio

---

## 📊 Analysis

### 1️⃣ Performance Across Sentiment Regimes
Compared:
- Average PnL
- Win rate
- Volatility proxy (PnL standard deviation)

### 2️⃣ Behavioral Changes
Analyzed:
- Trade frequency during Fear vs Greed
- Leverage usage differences
- Long/Short bias shifts

### 3️⃣ Trader Segmentation
Identified segments such as:
- High leverage vs Low leverage traders
- Frequent vs Infrequent traders
- Consistent vs Inconsistent performers

---

## 🔍 Key Insights

1. Trader performance differs significantly between Fear and Greed regimes.
2. High leverage usage tends to increase during Greed periods.
3. Trade frequency increases during Greed but average win rate may decline.
4. High leverage traders experience larger drawdowns during Fear periods.

---

## 💡 Strategy Recommendations

1️⃣ Dynamic Leverage Adjustment  
Reduce leverage exposure during Fear days to minimize drawdowns.

2️⃣ Controlled Trade Frequency  
Limit overtrading during Greed periods to protect win rate stability.

---

## 🚀 Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn (optional modeling)

---

## 📎 How to Run

1. Clone the repository
2. Install dependencies: