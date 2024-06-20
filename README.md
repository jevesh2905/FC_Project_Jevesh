# Stock Sentimental Analysis Project

This project focuses on sentiment analysis for a specific set of stocks and utilizes this analysis to develop a trading model that helps predict stock price behavior and informs trading decisions.

## Objective

The main objective is to perform sentiment analysis on news headlines for selected stocks and create a trading model to predict buy and sell points based on sentiment and historical data.

## Project Workflow

### 1. Data Collection

- *Web Scraping*: Data is scraped from [marketinsider.com](https://www.marketsinsider.com) using beautifulsoup.
- *Historical Data*: Downloaded from Yahoo Finance.

### 2. Data Preprocessing

- *Cleaning*: Headlines are tokenized, lowercased, and cleaned using NLTK.
- *Grouping*: Headlines are grouped by date.

### 3. Feature Engineering

- *Readability Score*: Flesch Reading Ease score.
- *Word Frequency*: Number of tokens in headlines.
- *Entity Ratio*: Ratio of named entities to total words using spacy.
- *Subjectivity*: Degree of personal opinion using TextBlob.
- *Polarity*: Sentiment score ranging from -1 (negative) to +1 (positive) using TextBlob.

### 4. Sentiment Analysis

- *VADER Sentiment*: Calculates sentiment scores (positive, negative, neutral, compound).

### 5. Model Training

- *Models Used*: Linear Discriminant Analysis (LDA), Support Vector Machine (SVM), Gradient Boosting Classifier.
- *Training Process*:
  - Data split into training and test sets.
  - Features standardized.
  - Hyperparameter tuning using GridSearchCV.
  - Model evaluation using accuracy and classification report.

### 6. Trading Strategy

- *Momentum Trading Strategy*: Utilizes Gradient Boosting Classifier to identify buy and sell points.
- *Performance Metrics*:
  - Sharpe Ratio
  - Maximum Drawdown
  - Number of Trades
  - Win Ratio

## Results

The models provided decent accuracy with a moderate win ratio and Sharpe ratio. The momentum trading strategy showed better performance compared to other strategies tested.

## Drawbacks

- Profit margins were not significantly high.
- Risk involved as indicated by the maximum drawdown.

## References

1. [Market Insider](https://www.marketsinsider.com)
2. [Basic Blog for Sentiment Analysis Overview](https://blog.quantinsti.com/sentiment-analysis-trading/)

## Related Research

For more detailed insights and methodology, please refer to the research paper: [Sentiment Analysis for Financial News](https://arxiv.org/pdf/2404.14248).

## Author

Javesh Patwari  
Enrollment No: 23115103
