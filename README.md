**Air Passenger Forecasting**
**Project Overview**

This project aims to forecast the number of airline passengers using historical data through advanced time-series analysis techniques. The challenge is a standard time-series prediction problem where identifying and modeling trend, seasonality, and noise are essential to building accurate forecasting models.

Stationarity in Time-Series
For reliable statistical modeling, the time-series must be stationary. A stationary series maintains:
Constant mean across time.
Constant variance or standard deviation.
Time-invariant auto-covariance.

To check and enforce stationarity, the following steps were performed:
ADF (Augmented Dickey-Fuller Test) and KPSS Test applied to test stationarity.
Box-Cox Transformation applied to stabilize variance and eliminate non-stationarity.
The ADF test provides test statistics, critical values, and a p-value. If the test statistic is below the critical threshold or the p-value is sufficiently low, the null hypothesis of non-stationarity can be rejected.

**Trend and Seasonality**
Two main factors often cause non-stationarity: trend and seasonality. To handle these, time-series decomposition was performed using Error-Trend-Seasonality models:
Trend Component: Long-term growth or decline pattern.
Seasonal Component: Repetitive, cyclical fluctuations.
Residual Component: Random noise or unexplained variance.

**Decomposition Models**
Additive Model – used when variations are linear and stable over time.
Multiplicative Model – applied when variations grow or decline non-linearly with time.

**Forecasting Models Implemented**

The following forecasting models were used to capture different aspects of the data:
Holt-Winters Exponential Smoothing – handles level, trend, and seasonality simultaneously.
ARIMA (AutoRegressive Integrated Moving Average) – combines:
AR (p): dependence on lagged values.
I (d): differencing to achieve stationarity.
MA (q): dependence on past forecast errors.
SARIMA (Seasonal ARIMA) – extends ARIMA by including seasonal differencing and lags for improved accuracy on cyclic datasets.
The AR component captures correlation across time, the MA component smooths noise, and differencing ensures stable patterns over the forecast horizon.

**Key Takeaway**
By applying statistical tests, decomposition techniques, and advanced forecasting models (ARIMA, SARIMA, Holt-Winters), the project demonstrates a structured approach to accurate air passenger demand forecasting, suitable for real-world decision-making in the aviation industry.
