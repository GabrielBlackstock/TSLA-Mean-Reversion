### README

# Mean Reversion Trading Strategy

## Overview

This script implements a mean reversion trading strategy on Tesla (TSLA) stock using historical data. Mean reversion is a financial theory suggesting that asset prices and historical returns eventually revert to the long-term mean or average level of the entire dataset.

## Strategy Details

- Initial Cash Position: £1 million.
- Mean Reversion Score Calculation: We calculate a 7-day return as the mean reversion score, where a negative score suggests a potential upward reversion (Long position), and a positive score suggests a downward reversion (Short position).
- Trading Signals: 
  - Long: The score is negative, indicating the price is lower than the 7-day average and might increase.
  - Short: The score is positive, indicating the price is higher than the 7-day average and might decrease.
  - Hold: The score does not strongly indicate either, suggesting to maintain the current position.
- Backtesting**: The strategy's performance is evaluated by simulating the trading decisions based on historical data.

## Results

The script outputs:
- A data frame showing the Close price, Mean Reversion Score, Signal, Portfolio Value, and ROI for each day.
- The initial and final portfolio values and ROI.
- The Sharpe Ratio, a measure of the return earned more than a risk-free rate per unit of volatility or total risk.

```
                 Close  Mean_Reversion_Score Signal  Portfolio_Value    ROI
Date                                                                       
2024-01-02  248.419998                   NaN   Hold       1000000.00   0.00
...
2024-04-01  175.220001              0.002505  Short       1241425.87  24.14

Initial Portfolio Value: £1,000,000.00
Final Portfolio Value: £1,241,425.87
ROI: 24.14%
Sharpe Ratio: 2.1544100816493463
```

## Interpretation

- Mean Reversion Score: Indicates the stock's short-term return relative to its 7-day history. Positive values indicate a higher price than the recent average, suggesting a potential sell or short signal. Negative values suggest the opposite, indicating potential buy or long signals.
- Sharpe Ratio**: A high Sharpe ratio indicates a good risk-adjusted return, with this strategy achieving a Sharpe ratio of 2.15, suggesting a relatively high return per unit of risk.

