# S&P500 Time Series Analysis
## Executive Summary

Between 2014 and 2017, the S&P 500 demonstrated a general upward trend with some moderate volatility and temporary drawdowns. Strong recoveries followed key downturns, particularly during early 2016. Return distributions were non-normal and exhibited fat tails, indicating frequent extreme values. Our synthetic index showed sustained bullish behavior, with multiple bullish “golden cross” signals observed during the analysis period. While daily returns were stationary, prices were not—supporting the use of return-based models for forecasting. Volume data showed weak correlation with price moves. Seasonality was evident in day-of-week and monthly return patterns, including mild “January effects.”


## Time Series Insights 

### Trend and Overall Behavior

- Overall, the S&P 500 experienced a bullish trend during this period.
- The synthetic index showed strong upward momentum, especially in 2017.
- After a choppy 2015 and a pullback in early 2016, the market entered a sustained bull run throughout the remainder of 2016 and 2017.

### Volatility and Fluctuations

- Volatility was relatively modest overall, with spikes in early 2016 (market fears around global growth) and during brief corrections.
- Rolling 30-day standard deviation showed heightened volatility in Q1 2016 and stable behavior throughout 2017.
- Volatility dropped significantly in 2017, coinciding with a low-VIX environment.

### Seasonality & Calendar Effects

- Monday returns were consistently lower than Friday returns.
- The market exhibited mild “January effects,” with above-average returns in January months.
- Some monthly and quarterly patterns emerged: Q4 typically had stronger momentum than Q2.
- No significant difference in volume by weekday, though Mondays and Fridays tended to show slightly higher volatility.

### Market Shocks & Events

- A sharp decline in August 2015 coincided with the Chinese market selloff.
- Another drawdown occurred in January–February 2016 (concerns over oil prices and global recession fears).
- Each of these drawdowns recovered within 1–3 months.
- Large return z-scores (>3) matched well with global market stress periods.

### Correlation with Volume
- Correlation between daily returns and volume was low overall (~0.02 to 0.05).
- Spikes in volume typically followed—not preceded—large price movements.
- No evidence of predictive power in volume spikes alone for anticipating large returns.

### Return Distributions

- Daily returns were centered around 0.04% with a standard deviation of ~0.65%.
- Returns showed excess kurtosis and slight negative skew—meaning frequent extreme events (fat tails).
- Returns were not normally distributed (verified via histogram and statistical tests).

### Stationarity and Forecasting

- Price series were non-stationary, but daily returns passed the Augmented Dickey-Fuller (ADF) test for stationarity.
- Short-term return forecasting using ARIMA performed better than naive random walk models, but predictive power remained low.
- Best forecasts were directional, not point-precise.

### Moving Averages and Signals

- The synthetic index's 50-day SMA crossed above the 200-day SMA (“golden cross”) in mid-2016 and stayed above through 2017.
- No bearish “death cross” patterns were observed during the analysis window.
- These crossover points coincided with stronger market performance.

### Risk Metrics

- Maximum drawdown (peak-to-trough decline) was approximately −7.1%, observed during early 2016.
- Annualized Sharpe ratio for the synthetic index was ~0.96, assuming a 0% risk-free rate.
- Volatility-adjusted performance improved steadily over the period.

### Recommendations

- Use return-based time series (not price) for modeling and forecasting due to stationarity.
- Incorporate moving average crossovers with volatility measures for strategy signals.
- Watch for early-year (January) momentum and weekday anomalies as potential trading cues.
- Consider stress-testing portfolios with fat-tailed distributions rather than assuming normal returns.
- Be cautious in relying on volume for predictive signals—combine it with price and volatility filters.


## Assumptions & Caveats

- The synthetic index is equally weighted—not market-cap-weighted like the real S&P 500.
- Corporate actions (splits/dividends) may not be fully adjusted in prices.
- Risk-free rate assumed to be 0 for Sharpe ratio calculations.
- Forecasting models were univariate and not trained on macroeconomic features or external signals.
- Not all stocks had complete data across all days (missing data filtered).
