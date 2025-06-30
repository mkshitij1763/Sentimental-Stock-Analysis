# 📈 Stock Sentiment Analysis Using Machine Learning

**Finance Club, IIT Roorkee**
*May 2023 – June 2023*

## Overview

This project explores the relationship between financial news sentiment and stock price movements. We developed a machine learning pipeline that combines NLP-based sentiment analysis with quantitative indicators (PE and DE ratios) to predict stock movements and evaluate investment returns. The model achieved **28% returns**, outperforming traditional benchmarks.

---

## 🔍 Problem Statement

Financial markets are heavily influenced by news. Accurately gauging sentiment from news articles can enhance stock prediction models. This project aims to integrate sentiment analysis with financial indicators to make informed predictions about stock performance.

---

## 💡 Approach

### 1. **Data Collection**

* Scraped financial news from:

  * [Financial Times (FT)](https://www.ft.com)
  * [Economic Times (ET)](https://economictimes.indiatimes.com)
  * [New York Times (NYT)](https://www.nytimes.com)
* Tools Used: `BeautifulSoup`, `requests`

### 2. **Sentiment Analysis**

* Model: [RoBERTa-base](https://huggingface.co/roberta-base)
* Extracted sentiment scores for each article (positive, negative, neutral)

### 3. **Quantitative Analysis**

* Financial indicators used:

  * Price-to-Earnings (PE) ratio
  * Debt-to-Equity (DE) ratio
* Data Sources: Yahoo Finance, Alpha Vantage

### 4. **Modeling**

* ML Algorithm: `XGBoost` classifier
* Features: Sentiment scores + PE + DE + moving averages
* Training Set: TSLA (Tesla), GM (General Motors)
* Test Set: Ford (F)

### 5. **Evaluation**

* **Accuracy:** 85% on test set
* **Returns:** 28% return on test portfolio simulation
* Benchmarked against S\&P 500 and other baseline models

---

## 📊 Results

| Metric         | Value                                  |
| -------------- | -------------------------------------- |
| Accuracy       | 85%                                    |
| Returns        | +28%                                   |
| Model Used     | RoBERTa + XGBoost                      |
| Backtest Stock | Ford (F)                               |
| Evaluation     | Sentiment accuracy + Return comparison |

---

## 🧰 Technologies & Libraries

* Python
* BeautifulSoup
* `transformers` (Hugging Face)
* XGBoost
* `scikit-learn`
* `matplotlib`, `seaborn` (for visualization)
* Jupyter Notebook

---

## 📁 Project Structure

```
├── data/                   # Raw and processed datasets
├── notebooks/              # Jupyter notebooks with code
├── models/                 # Trained model artifacts (if stored)
├── finance_analysis.ipynb  # Main notebook
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

---

## 🚀 Getting Started

### Installation

```bash
git clone https://github.com/mkshitij1763/stock-sentiment-analysis.git
cd stock-sentiment-analysis
pip install -r requirements.txt
```

### Run the notebook

```bash
jupyter notebook finance_analysis.ipynb
```

---

## ✅ Future Work

* Add more diverse news sources
* Experiment with LSTM and BERT variants
* Include macroeconomic indicators (GDP, inflation)
* Real-time dashboard for stock alerts

---

