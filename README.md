# RandomForest_ROIxLockPeriod
Calcule via random forest method the expected selling pressure based on ROI &amp; Dormancy (Lock period)


# Token Vesting Simulation and Black-Scholes Price Dynamics

This repository contains a Python script that simulates token vesting schedules and token sale probabilities based on price trajectories modeled with Black-Scholes dynamics. The simulation incorporates vesting schedules, dormancy periods, and machine learning-based sell probability predictions to assess the behavior of token holders under various scenarios.

## Features

- **Black-Scholes Price Simulations**:
  - Simulates price dynamics for a given number of runs using drift, volatility (sigma), and a starting price.
  - Filters out extreme price jumps (e.g., >50x the starting price).

- **Sell Probability Modeling**:
  - Uses a machine learning model (`rf_model_sale.pkl`) to predict sell probability based on ROI (Return on Investment) and dormancy.
  - Adds Gaussian noise to simulate real-world variability.

- **Vesting Schedule Integration**:
  - Computes sell probabilities, tokens sold, and tokens held for each unlock event.
  - Redistributes unsold tokens in subsequent unlock events.

- **Monte Carlo Simulations**:
  - Simulates thousands of price trajectories to calculate median, quartiles, and probabilities.

- **Visualizations**:
  - Cumulative tokens sold over time.
  - Scatter plot of Sell Probability vs Dormancy.
  - Price probability cone (median, quartiles).
  - Sell Probability and Median Price on unlock days.

## Requirements

- Python 3.x
- Required Libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn` (for loading the machine learning model)
  - `openpyxl` (for reading Excel files)

Install the required dependencies using:
```bash
pip install -r requirements.txt
