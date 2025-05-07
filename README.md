# Modeling for Temperature Forecasting and Prediction Markets 
 University of Notre Dame

This project explores the relationship between weather-based prediction markets and actual temperature outcomes. Our team applied time series forecasting techniques to predict daily high temperatures in New York City and assess whether Polymarket’s market-implied probabilities align with real-world data. The project was completed as part of the MSBA Time Series Forecasting course at the University of Notre Dame.

## Team
 
- Alex Heck – [@aheck3](https://github.com/aheck3)  
- Tim McDonald – [@tmcdona](https://github.com/tmcdona)  
- Cooper Foster – [@coopfos](https://github.com/coopfos)  

Professor: Dr. Sriram Somanchi  
Date: February 2025  

## Objective

The primary objective was to determine whether traders in Polymarket’s weather-based prediction markets are accurately pricing contracts based on real temperature probabilities — or whether opportunities exist for informed traders to profit from mispricings.

We forecasted next-day high temperatures in NYC using a range of time series models and simulated trades on Polymarket based on those predictions.

## Models Applied

- **Naïve Forecast**  
- **Seasonal Naïve Forecast**  
- **Linear Regression**  
- **ARIMA (AutoRegressive Integrated Moving Average)**  
- **Neural Network Autoregression**

Each model’s performance was evaluated using error metrics and hypothetical profit/loss from simulated Polymarket trades.

## Data

- `LGA_temps.xlsx`: Raw temperature data collected from LaGuardia Airport (New York City)
- `updated_set.csv`: Cleaned and preprocessed temperature dataset used for model training and forecasting

Both datasets were cleaned and preprocessed to ensure modeling accuracy.

## Key Findings

- **ARIMA and Naïve models** delivered the strongest forecasting and trading performance, outperforming alternative methods like neural nets and linear regression.
- **Seasonal models underperformed**, likely due to an anomalously cold U.S. winter that broke expected temperature patterns.
- Simulated trades based on our forecasts **generated positive returns** for some models — suggesting that Polymarket contract prices do not always reflect true temperature probabilities.

**Model Validation: Hypothetical Profit/Loss**  
_Assumes $100 simulated bet placed per model prediction, purchased at best available price near 6 PM the day before each market expired._

| Model          | Winnings | Losses   | Net P/L  |
|----------------|----------|----------|----------|
| Naïve          | $12,471  | $(2,100) | $10,371  |
| Seasonal Naïve | $9,382   | $(2,600) | $6,782   |
| Linear Mod     | $231     | $(2,600) | $(2,369) |
| ARIMA          | $12,380  | $(2,200) | $10,180  |
| Neural Net     | $1,123   | $(2,600) | $(1,477) |


## Methodology

1. **Validation Split**: Jan 22 – Feb 21, 2025 was used for out-of-sample validation.
2. **Rolling Validation**: For ARIMA and NN tuning, multiple rolling splits were used.
3. **Profit Simulation**: Each model's daily forecast was used to simulate a “trade” $100 on the predicted contract.
4. **Performance**: Measured using RMSE, MAE, and simulated trading profit/loss.

## Files Included

- `nyc-temperature-forecasting-analysis.Rmd` – R Markdown file with full modeling code  
- `forecasting-polymarket-temp-report.pdf` – Written report and results summary  
- `forecasting-polymarket-temp-presentation.pdf` – Presentation slides  
- `data/` – Includes:
  - `LGA_temps.xlsx` – Daily high temperatures
  - `updated_set.csv` – Cleaned modeling dataset  
- `images/` – Plots and charts used in the report  

> **Note**: An `.html` version of the report is not included, but the `.Rmd` and `.pdf` files are both available for reproducibility and reference.

## Conclusion

This project demonstrates that even relatively simple models can provide value in forecasting and market prediction. By combining time series forecasting with economic insight, informed participants may be able to spot inefficiencies in emerging blockchain-based markets like Polymarket.

## Report

📄 [Click here to view the full report (PDF)](forecasting-polymarket-temp-report.pdf)

## Acknowledgments

Thanks to my fellow researchers:
- [@tmcdona](https://github.com/tmcdona) - MSBA
- [@coopfos](https://github.com/coopfos) - MSBA 

And thank you to Professor Sriram Somanchi for guiding us through this time series forecasting course at the University of Notre Dame.  
I truly enjoyed the lectures and the techniques we explored throughout the term.

---

