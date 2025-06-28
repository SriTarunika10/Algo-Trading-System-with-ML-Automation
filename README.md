# Algo-Trading-System-with-ML-Automation
This project is a modular, Python-based **Algorithmic Trading System** that uses technical indicators and machine learning to generate BUY signals for NIFTY 50 stocks, logs them to **Google Sheets**, and sends real-time alerts via **Telegram**.

---

## 🔍 Features

- 📡 **Real-time Stock Data** from Yahoo Finance (`yfinance`)
- 📉 **Strategy Logic**: RSI + Moving Average Crossover
- 🧠 **ML Prediction**: Logistic Regression to predict next-day movement
- 📊 **Interactive Streamlit UI** with charts and metrics
- ✅ **Google Sheets Logging**: Auto-log trade signals & PnL
- 📬 **Telegram Integration**: Daily trade alerts
- 📁 **Modular Codebase**: Clean and scalable

---

## 📦 Folder Structure

│
├── main.py # Main Streamlit App
├── fetch_data.py # Fetches data from Yahoo Finance
├── strategy.py # Trading strategy logic
├── ml_model.py # ML model for predictions
├── gsheet_logger.py # Google Sheets logging
├── telegram_bot.py # Telegram message sender
├── credentials.json # Google Sheets API credentials (not included in repo)
├── requirements.txt # Python dependencies
└── README.md # You're here!

## 🚀 How to Run

1. **Install dependencies**
   ```bash
   pip install -r requirements.txt

2. **Add Google Sheets credentials**

'''Place your credentials.json file in the root folder.

Share the sheet with your Google service email.

3. **Run the Streamlit app**

*streamlit run app.py*



## ⚙️ Strategy Logic

**BUY Signal is triggered when:**

- 📉 RSI < 30 (indicating oversold condition)
- 🔀 20-DMA (Daily Moving Average) crosses **above** 50-DMA (bullish crossover)

**🧠 ML Model Integration**

- Uses **Logistic Regression** to predict next-day movement (`Up` or `Down`)
- Features include:
  - RSI
  - Volume
  - Price change indicators
- Outputs:
  - Predicted movement
  - Accuracy score for each stock

---

## 📬 Telegram Alerts

Each day, a formatted Telegram message is sent like this:


