# 📈 Stock Price Prediction Using NLP and Sentiment Analysis

This project uses **Natural Language Processing (NLP)** and financial sentiment analysis to predict Microsoft (MSFT) stock prices. By combining human-labeled sentiment data, a transformer-based FinBERT model, and historical stock prices, we train a machine learning model to estimate future closing prices.

---

## 🛠️ Tools & Technologies
- **FinBERT**: Transformer model fine-tuned for financial sentiment
- **Takala Financial PhraseBank**: Human-labeled financial sentiment dataset
- **yfinance**: For downloading historical MSFT stock data
- **scikit-learn**: Linear Regression model and evaluation metrics
- **pandas**, **NumPy**, **matplotlib**: Data handling and visualization
- **datasets**: From HuggingFace, used to load the PhraseBank

---

## 🔍 What the Project Does

- Extracts financial sentences and their sentiment labels from the PhraseBank dataset
- Applies FinBERT to each sentence to get sentiment predictions
- Simulates news publishing dates and aligns sentiment data with historical stock data
- Creates feature sets including:
  - Previous day's closing stock price
  - Average PhraseBank sentiment score per day
  - Average FinBERT sentiment score per day
- Trains a **Linear Regression model** to predict the next day's MSFT closing price
- Evaluates performance using MAE, RMSE, and R²
- Visualizes predicted vs. actual prices over time

---

## 🧪 Model Performance

| Metric | Score   |
|--------|---------|
| MAE    | ~3.71   |
| RMSE   | ~4.58   |
| R²     | **0.9232** ✅ |

> The model explains ~92% of the variation in MSFT's closing price using sentiment and previous-day price data.

---

## 📊 Sample Output

![Prediction vs Actual Plot](<INSERT_PATH_TO_YOUR_PLOT_IMAGE>)

---

## ⚠️ Limitations and Future Improvements

While the model performs well, there are several opportunities to improve:

- **Add more features**: Trading volume, macroeconomic indicators, technical signals
- **Use real-time sentiment**: Connect with news APIs or social media feeds
- **Try advanced models**: Random Forests, XGBoost, or LSTM for time-series
- **Use lagged or rolling features**: To capture multi-day sentiment trends
- **Refine alignment**: Better match between actual news timestamps and market movements

---

## ✨ Future Directions

- Integrate real-time news and intraday stock data
- Explore causality between specific news events and stock changes
- Extend the framework to other stocks or financial instruments
- Compare multiple sentiment models (e.g., FinBERT vs. RoBERTa)

---

## 📌 Disclaimer

This project is intended for educational purposes only. The model is not a financial forecasting tool and should not be used for investment decisions.

---

## 📬 Contact

Have questions or ideas? Feel free to open an issue or contact me directly.


