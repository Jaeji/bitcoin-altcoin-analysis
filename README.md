# Bitcoin Cryptocurrency Analysis

An applied cryptocurrency market analysis project examining the relationship between Bitcoin and selected altcoins using clustering, directional causality testing, and return forecasting.

## Project Objectives

- Explore return, volatility, and correlation patterns across cryptocurrencies.
- Identify groups of altcoins with similar market characteristics.
- Examine whether past Bitcoin returns help explain subsequent altcoin returns.
- Compare forecasting approaches for one-step-ahead log returns.

## Methodology

1. **Data Preparation** – Sort timestamps, remove duplicate observations, inspect missing values, and prepare hourly or minute-level price data.
2. **Exploratory Analysis** – Calculate log returns, test stationarity using the Augmented Dickey-Fuller (ADF) test, and examine correlations and rolling volatility.
3. **Clustering** – Apply K-Means and Ward hierarchical clustering using mean return, volatility, and correlation with Bitcoin.
4. **Directional Causality** – Use VAR lag selection and Granger causality tests to examine the direction from Bitcoin to selected altcoins.
5. **Return Forecasting** – Compare OLS, XGBoost, and LSTM models for one-step-ahead log-return prediction.
6. **Evaluation** – Evaluate forecasts using error metrics on log returns and reconstructed prices, with baseline comparisons.

## Tools & Technologies

- Python
- pandas, NumPy
- statsmodels
- scikit-learn
- XGBoost
- TensorFlow / Keras
- Jupyter Notebook

## Repository Contents

- `bitcoin_altcoin_analysis.ipynb` – Main analysis notebook.
- `requirements.txt` – Python package dependencies.
- `data/` – Directory for the input price dataset (not included).

## How to Run

```bash
pip install -r requirements.txt
```

Place the input price CSV in the `data/` directory and update `DATA_FILE` in the notebook configuration cell. Then run the notebook from top to bottom.

**Note:** Full model tuning, particularly the LSTM search, may require substantial computation time.

## Notes

The project focuses on statistical relationships and predictive experiments. Granger causality indicates predictive precedence under the selected model specification; it does not by itself establish economic causation.
