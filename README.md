# Demonstration-Value-at-Risk-in-Python

# Value at Risk (VaR) Analysis

## Overview

This project implements three widely-used methods for calculating **Value at Risk (VaR)** on a diversified portfolio of 12 stocks. VaR is a statistical measure that quantifies the potential loss in portfolio value over a specified time period at a given confidence level, making it essential for risk management and investment decision-making.

## What is Value at Risk?

Value at Risk answers the question: *"What is the maximum amount I could lose on my portfolio over the next N days with X% confidence?"*

For example, a 95% VaR of $42,751 over 5 days means there is only a 5% chance that the portfolio will lose more than $42,751 in the next 5 trading days.

## Portfolio Composition

The analysis uses a $1,000,000 equally-weighted portfolio consisting of:
- **Technology**: TTWO, PLTR, PSKY, AAPL, NVDA, SHOP
- **Finance**: BLK, JPM, HOOD
- **Consumer**: T, WMT, RL

Historical data spans 2 years of daily closing prices.

## Three VaR Methods Implemented

### 1. **Monte Carlo Simulation**
- Simulates 10,000 possible portfolio scenarios using random sampling
- Assumes returns follow a normal distribution
- Most flexible approach, can model complex risk factors

### 2. **Historical Method**
- Uses actual historical returns to estimate future risk
- No distributional assumptions required
- Based on 5-day rolling window analysis

### 3. **Parametric Method (Variance-Covariance)**
- Assumes returns are normally distributed
- Uses portfolio mean and standard deviation
- Fastest computation, analytical solution

## Key Results (5-Day Horizon)

| Method | 90% VaR | 95% VaR | 99% VaR |
|--------|---------|---------|---------|
| **Monte Carlo** | $31,256 | $42,751 | $64,399 |
| **Historical** | $27,455 | $41,420 | $84,273 |
| **Parametric** | $41,485 | $53,246 | $75,306 |

## Technologies Used

- **Python 3.x**
- **yfinance**: Real-time financial data retrieval
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computations
- **scipy**: Statistical functions and distributions

