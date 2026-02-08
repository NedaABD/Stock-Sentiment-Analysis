# Stock-Sentiment-Analysis
# Stock Market Sentiment Analysis Using Twitter Data

## Overview
This project analyzes the relationship between **public sentiment on Twitter** and **stock market behavior**. It collects tweets related to specific stocks, applies **sentiment analysis** using multiple NLP techniques, and compares sentiment trends with **real stock price data** retrieved from financial APIs.

The goal is to explore how **social media sentiment** aligns with or reacts to market movements using an end-to-end data pipeline.

---

## Features
- Twitter data collection using the Twitter API
- Text preprocessing and cleaning
- Sentiment analysis using:
  - VADER
  - TextBlob
- Real-time stock price retrieval using Yahoo Finance
- Data visualization and exploratory analysis
- Modular Python pipeline for experimentation

---

## Project Structure
```
.
├── main.py                     # Entry point for running the pipeline
├── twitter_tweet_Extraction.py # Collects tweets using Twitter API
├── data_pre_processing.py      # Cleans and preprocesses tweet text
├── sentiment_analysis.py       # Sentiment analysis controller
├── vader_sentiment.py          # VADER-based sentiment scoring
├── textblob_sentiment.py       # TextBlob-based sentiment scoring
├── getSentiment.py             # Aggregates sentiment results
├── getRealStock.py             # Fetches real stock data via yfinance
├── test.py                     # Testing and experimentation
├── requirements.txt            # Project dependencies
└── README.md
```

---

## Requirements
- Python 3.8+
- Twitter Developer API access

Install dependencies:
```bash
pip install -r requirements.txt
```

---

## Data Sources
- **Twitter API**: Tweets related to selected stock tickers
- **Yahoo Finance (yfinance)**: Historical and real-time stock prices

---

## Usage

1. **Configure Twitter API credentials**  
   Add your API keys inside `twitter_tweet_Extraction.py`.

2. **Run the main pipeline**
```bash
python main.py
```

This will:
- Collect tweets for a given stock
- Clean and preprocess text
- Compute sentiment scores
- Fetch corresponding stock price data
- Produce outputs for analysis and visualization

---

## Sentiment Analysis Methods

### VADER
- Lexicon and rule-based sentiment model
- Optimized for social media text
- Produces positive, negative, neutral, and compound scores

### TextBlob
- Polarity-based sentiment scoring
- Simpler linguistic sentiment model
- Used for comparison with VADER results

---

## Output
- Cleaned tweet datasets
- Sentiment scores per tweet
- Aggregated sentiment trends
- Stock price time series
- Visualizations comparing sentiment and price movement

---

## Limitations
- Twitter sentiment may be noisy or biased
- No causal relationship is assumed between sentiment and price
- Limited by Twitter API rate limits
- Market movements influenced by many external factors

---

## Future Improvements
- Use transformer-based sentiment models (e.g., BERT)
- Add time-lag analysis between sentiment and price
- Expand to multiple stocks and sectors
- Deploy as a web dashboard using Flask
- Incorporate news articles alongside tweets

---

## Acknowledgments
This project was developed as an academic exploration of **NLP, social media analytics, and financial data analysis** using Python.
