# 🛒 Store Sales Forecasting

This project forecasts daily sales across Ecuadorian grocery stores using historical data and external signals. I built and compared two models — a baseline linear regression and a more expressive XGBoost regressor — to capture seasonality, promotions, and holiday effects.

## 📁 Data Sources
- `train.csv`: historical sales data
- `stores.csv`: store metadata
- `oil.csv`: daily oil prices
- `holidays_events.csv`: national and regional holidays

## 🧠 Feature Engineering
- Calendar features: day of week, month, year
- Lagged sales: 7-day and 14-day lags
- Rolling averages: 7-day mean
- Holiday flags and store/product encodings

## 📊 Model Comparison
| Model             | RMSLE (Aug 1–15, 2017) |
|------------------|------------------------|
| Linear Regression| 3.0054                 |
| XGBoost          | 0.5353                 |

## 🔍 Key Insights
- Lag and rolling features dominate predictive power
- XGBoost captures nonlinear and temporal patterns far better than linear regression
- Feature importance shows strong reliance on recent sales trends

## 🚀 Next Steps
- Add SHAP values for interpretability
- Explore per-store modeling or grouped time series
- Deploy as a forecasting API or dashboard

## 📄 License

This project is licensed under the MIT License.  
Note: The datasets used are from the [Store Sales Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting) competition on Kaggle and are not redistributed here. To access the data, please visit the official competition page.
