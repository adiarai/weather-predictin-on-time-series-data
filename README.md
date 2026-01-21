<img width="568" height="414" alt="ad6" src="https://github.com/user-attachments/assets/fb885ae1-fa89-475f-b985-5937468d5a40" />
Weather Prediction Using Recurrent Neural Networks
Project Description

This project demonstrates how to use Recurrent Neural Networks (RNNs) to predict future weather temperatures based on historical time-series data. By leveraging hourly weather measurements and temporal patterns, the model learns to forecast temperature trends, highlighting the power of deep learning for time-dependent data.

The dataset includes meteorological measurements such as temperature, pressure, humidity, and other environmental features collected in Jena, Germany from 2009 to 2016.

The project illustrates practical skills in data preprocessing, feature engineering, normalization, sequence generation, RNN modeling, prediction, and visualization.

Dataset

Source: jena_climate_2009_2016.csv

Number of observations: ~420,551 (resampled to 70,091 for hourly data)

Features include:

p (mbar): Atmospheric pressure

T (degC): Temperature (target variable)

Tpot (K): Potential temperature

Tdew (degC): Dew point

rh (%): Relative humidity

VPmax (mbar), VPact (mbar), VPdef (mbar): Vapor pressure

sh (g/kg): Specific humidity

H2OC (mmol/mol): Water vapor concentration

rho (g/m³): Air density

Removed features: wv (m/s), max. wv (m/s), wd (deg) due to low predictive relevance

Key Features

Time Series Prediction: Temperature forecast based on past weather observations.

Feature Engineering: Added sinusoidal transformations (Day sin, Day cos, Year sin, Year cos) to encode daily and seasonal patterns.

Data Normalization: Standardized training data and applied same scaling to validation and test sets.

RNN Modeling: Used LSTM layers for capturing sequential dependencies in time-series data.

Evaluation Metrics: Mean squared error (MSE) to assess prediction accuracy.

Visualization: Plot actual vs predicted temperatures to evaluate model performance.

Findings from Analysis

From the model and analysis, we found:

Daily and Seasonal Patterns Matter: Incorporating sinusoidal features representing daily and yearly cycles significantly improved the model’s ability to capture temperature trends.

RNN Captures Temporal Dependencies: The LSTM model successfully learned patterns in hourly temperature changes, providing predictions closely aligned with actual temperatures.

Prediction Accuracy: The model achieved low mean squared error, indicating reliable short-term temperature forecasting.

Feature Importance: Variables such as pressure (p), humidity (rh), and dew point (Tdew) were strongly correlated with temperature, while wind-related features had low predictive value and were removed.

Visualization Insights: Plotting predicted vs actual temperatures revealed that the model effectively follows temperature fluctuations but may slightly lag during sudden rapid changes, which is expected in real-world weather data.

Conclusion: This analysis confirms that RNNs, combined with thoughtful feature engineering, can effectively predict temperature trends in time-series weather data. The approach can be extended to other environmental metrics or locations with similar temporal patterns.
