# HFT Backtesting Engine

This repository contains a High-Frequency Trading (HFT) backtesting engine built in Python. The system applies a mean reversion strategy using Bollinger Bands, RSI, and configurable Stop Loss / Take Profit thresholds to evaluate tick-level trading data.

## Overview

The project was built as an individual effort to understand and implement the logic behind a robust backtesting system on real tick data. It walks through a complete pipeline — from **data collection** to **cleaning**, **technical indicator generation**, **strategy implementation**, and finally, **visualization and optimization**.

Two Jupyter notebooks are provided:

- **`backtesting.ipynb`**: This is the **main development notebook** that includes every stage of experimentation — raw logic development, trial runs, commentary, and visualization. It reflects the full thought process and learning.
  
- **`backtesting_final_code.ipynb`**: This is the **cleaned and organized final version**, showing only the optimized version of the strategy along with a basic parameter tuning UI for visualizing results.

## Strategy Logic

The implemented strategy uses:

- **Bollinger Bands** for identifying mean-reverting opportunities.
- **RSI (Relative Strength Index)** to filter trades during oversold and overbought conditions.
- **Stop Loss** and **Take Profit** levels to manage trade exits.
- Performance is measured using final portfolio value, number of trades, and **Sharpe Ratio**.

Optimization is done on the rolling window size for Bollinger Bands to identify the best-performing configuration.

## UI & AI Collaboration

The final notebook includes an interactive UI built using `ipywidgets` to allow users to dynamically change parameters like the rolling window, RSI thresholds, and SL/TP limits.

> **Note**: The UI section was integrated using code generated with the help of AI tools. This was a purposeful experiment to test whether modern AI can accelerate coding workflows for longer interactive scripts — a relevant skill today with tools like Cursor, GitHub Copilot, Lovable and ChatGPT. All backtesting logic and strategy implementation, however, were coded by me directly.

## Files

| File | Description |
|------|-------------|
| `backtesting.ipynb` | Full project notebook with step-by-step logic, trials, and all stages |
| `backtesting_final_code.ipynb` | Final organized version with parameter tuning UI |
| `cleaned_data.parquet` | Cleaned tick data used for backtesting |
| `VOL.IDXUSD_Ticks_24.03.2025-24.03.2025.csv` | Raw tick data |
| `README.md` | This documentation |

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- ipywidgets
- Jupyter Notebook
