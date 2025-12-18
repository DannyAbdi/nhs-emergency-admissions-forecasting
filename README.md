# NHS Emergency Admissions Forecasting

## Overview
This project forecasts monthly NHS emergency admissions in England using publicly available
NHS England data. The goal is to demonstrate an end-to-end time series forecasting workflow
with a focus on realistic baselines and model evaluation.

## Data
- Source: NHS England A&E Attendances and Emergency Admissions (monthly time series)
- Granularity: Monthly
- Geography: England
- Target variable: Total Emergency Admissions

## Methods
- Baseline models: Naive, Seasonal Naive
- Statistical model: SARIMA
- Machine learning model: Random Forest with lag features
- Evaluation: Time-based validation split, MAE and RMSE

## Results
The Seasonal Naive baseline achieved the lowest validation error (MAE ≈ 7,800 admissions/month),
highlighting strong annual seasonality in NHS emergency admissions. More complex models did not
consistently outperform this benchmark without additional external variables.

## Key Takeaways
- Strong yearly seasonality dominates NHS emergency admissions
- Simple baselines can outperform complex models
- Forecasting accuracy at national scale is limited without exogenous drivers

## Future Work
- Incorporate external factors (flu incidence, weather, holidays)
- Rolling-origin cross-validation
