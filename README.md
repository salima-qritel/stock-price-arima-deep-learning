# 📈 Time Series Forecasting of Apple Stock Price Using ARIMA and Deep Learning Models

## 📌 Project Description
This project focuses on **analyzing and predicting Apple Inc. stock prices** using historical data from 1980 to 2022.  
It combines **time series models (ARIMA)** and **deep learning approaches (ANN, LSTM)** to capture trends, seasonality, and volatility.  

The goal is to compare different forecasting techniques and highlight insights for financial analysis and decision-making.

---

## 📊 Dataset
- **Name**: Apple Stock Price (1980–2022)  
- **Source**: [Yahoo Finance]  
- **Records**: 10,468  
- **Columns**:
  - `Date`: Record date  
  - `Open`: Opening price  
  - `High`: Daily high  
  - `Low`: Daily low  
  - `Close`: Closing price  
  - `Adj Close`: Adjusted close (splits/dividends)  
  - `Volume`: Trading volume  

---

## ⚙️ Data Preprocessing
- Converted `Date` column to **datetime** and set as index  
- Detected and removed **outliers** (±1.5 std)  
- Resampled to **weekly frequency**  
- Removed missing values and duplicates  
- Normalized with **MinMaxScaler** for deep learning models  

---

## 🔎 Exploratory Data Analysis
- **Visualization of closing prices** over 40 years  
- **ADF test** → data is non-stationary  
- **Time series decomposition** → trend, seasonality, residuals  
- Strong **growth after 2010** and **increased volatility post-COVID-19**  

---

## 🤖 Modeling

### 1️⃣ ARIMA (AutoRegressive Integrated Moving Average)
- Parameter tuning with **Grid Search**  
- Best model: **ARIMA(1,1,4)** with AIC = -2314  
- Evaluation: RMSE ≈ **0.86** (better than baseline)  

### 2️⃣ ANN (Artificial Neural Network)
- Dense layers with **Dropout** for regularization  
- Input: 30-day sequences → output: next-day prediction  
- Results:  
  - RMSE: **3.64**  
  - R²: **0.90**  

### 3️⃣ LSTM (Long Short-Term Memory)
- Sequential LSTM layers with Dropout  
- Able to capture long-term temporal dependencies  
- Outperformed ANN with better generalization  

---

## 📊 Results & Comparison
- **ARIMA**: Strong for trend modeling, limited for non-linear patterns  
- **ANN**: Good performance, but sensitive to volatility  
- **LSTM**: Best trade-off, robust for complex sequential dependencies  

---

## 📦 Technologies Used
- **Python 3.10+**
- Main libraries:
  - `numpy`, `pandas`, `matplotlib`, `seaborn`, `plotly`
  - `statsmodels` (ADF, ARIMA)
  - `scikit-learn` (scaling, metrics)
  - `tensorflow / keras` (ANN, LSTM)

---

## 🚀 How to Run
1. Clone the repository  
   ```bash
   git clone https://github.com/username/apple-stock-prediction.git
   cd apple-stock-prediction
   ```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Run Jupyter Notebook or Python script
```bash
jupyter notebook
```

or
```bash
python main.py
```
## 📌 Conclusion

- Apple stock shows a long-term upward trend.

- Deep learning models, especially LSTM, outperform ARIMA in predictive accuracy.

- This project can be extended to other stocks or adapted into a predictive trading system.

## ✨ Author

👤 Developed by Salima-qritel 

]
