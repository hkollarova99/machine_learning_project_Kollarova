# Machine Learning Project: Stock Volatility Prediction
Hana Kollárová, Jan 2026

This project aims to predict stock volatility using machine learning methods. Volatility was chosen as it is a more feasible task than actual stock price predictions. 

## Part 1: Single Stock Analysis (AAPL)

The first part is divided into four phases:
1. **Data Collection** (`1-Data_Collection`) - Downloading AAPL stock data from Yahoo Finance
2. **Feature Engineering** (`2-Feature_Engineering`) - Creating technical indicators and volatility features
3. **Model Training** (`3-Model_Training`) - Training Ridge Regression, Random Forest, and XGBoost models
4. **Evaluation** (`4-Evaluation`) - Testing on held-out data and analyzing results

Three machine learning models were used: Linear regression with regularisation, random forests, and XGBoost. These were chosen because they are standard ML models. In real life, most finance people use GARCH models (Generalised Autoregressive Conditional Heteroskedasticity), which are specifically designed for volatility. However, as this method borders more on econometrics than ML, a more standard approach was taken.

## Part 2: Multi-Stock Comparative Analysis

The second part extends the analysis to 5 stocks from diverse sectors to answer the research question:
**Does a general model trained on multiple stocks perform better than individual stock-specific models?**

### Stocks Analysed
- **AAPL** (Apple - Technology)
- **GOOGL** (Alphabet - Technology/Communication)
- **JPM** (JPMorgan Chase - Finance)
- **JNJ** (Johnson & Johnson - Healthcare)
- **XOM** (Exxon Mobil - Energy)

### Part 2 Phases
5. **Multi-Stock Collection** (`5-Multi_Stock_Collection`) - Downloading data for 4 additional stocks (same time period: 2022-2024)
6. **Multi-Stock Features** (`6-Multi_Stock_Features`) - Creating identical features for all stocks with consistent train/val/test splits
7. **Individual RF Models** (`7-Individual_RF_Models`) - Training one Random Forest model per stock
8. **Combined RF Model** (`8-Combined_RF_Model`) - Training a single RF model on all 5 stocks combined
9. **Model Comparison** (`9-Model_Comparison`) - Final evaluation comparing individual vs combined models on test sets

### Key Outputs (Part 2)
- `multi_stock_eda.png` - Exploratory data analysis for new stocks
- `multi_stock_features.png` - Feature correlations across stocks
- `individual_rf_models.png` - Individual model performance
- `combined_rf_model.png` - Combined model analysis
- `model_comparison.png` - Final head-to-head comparison

## Running this

### Requirements
- Python 3.8+
- pandas, numpy, matplotlib
- scikit-learn
- xgboost
- yfinance
- joblib

### Execution Order
**Part 1:** Run scripts 1 → 2 → 3 → 4 in sequence.

**Part 2:** Run scripts 5 → 6 → 7 → 8 → 9 in sequence.

Note: Part 2 depends on AAPL data from Part 1 being available.
