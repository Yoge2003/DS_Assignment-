# Trader Behavior Analysis Under Market Sentiment (Fear vs Greed)

## Overview

This project analyzes how trader behavior changes under different market sentiment conditions — specifically **Fear vs Greed** — using real trading data and market sentiment indicators. The goal is to understand how emotions influence **profitability, risk-taking, trade volume, costs, and timing**, and to derive **data-backed signals** that can support smarter trading decisions.

The analysis focuses on behavioral patterns rather than prediction, emphasizing **explainability and practical insights**.

## Problem Statement

Financial markets are heavily influenced by investor psychology. During periods of extreme fear or greed, traders often deviate from rational decision-making, leading to overtrading, excessive risk-taking, or missed opportunities.

This project addresses the following questions:

* How does profitability differ between Fear and Greed periods?
* Do traders take more risk during Greed?
* Does trading volume and frequency increase with optimism?
* Are losses and fees amplified during emotional market conditions?
* Can sentiment-aware behavior improve risk-adjusted performance?

## Data Sources

* **Market Sentiment Data**
  Daily Fear & Greed Index representing overall market psychology.

* **Trader Transaction Data**
  Historical trade-level data including execution price, position size, direction, fees, timestamps, and realized profit/loss.

Both datasets were merged at a daily level to align trader behavior with prevailing market sentiment.

## Methodology

1. **Data Cleaning & Preparation**

   * Converted timestamps to proper datetime formats
   * Extracted date and intraday features
   * Standardized sentiment into two groups: *Fear* and *Greed*

2. **Feature Engineering**

   * Trade size as a proxy for risk exposure
   * Profit/loss indicators
   * Hour-wise trading behavior
   * Fee aggregation to capture hidden costs

3. **Behavioral Analysis**

   * Profitability comparison (mean, median, win rate)
   * Risk analysis using position size and variability
   * Volume and participation analysis
   * Loss-focused analysis to study drawdowns
   * Directional bias (BUY vs SELL)
   * Intraday crowding patterns

4. **Visualization & Interpretation**

   * Distribution plots and comparative charts were used to validate insights visually.
   * All findings are supported by data, not assumptions.

## Key Insights

* **Greed periods show higher average profits**, but also **larger losses and higher volatility**.
* **Trade sizes and frequency increase significantly during Greed**, indicating aggressive risk-taking.
* **Transaction fees are substantially higher during Greed**, reducing net profitability.
* **Extreme losses are more frequent during Greed**, highlighting overconfidence risk.
* **Fear periods exhibit more controlled behavior** with better risk-adjusted outcomes.
* **Intraday analysis reveals crowding** during Greed at specific hours without consistent profitability.

## Trading Signals Identified

Based on data-backed analysis:

* Reduce position sizes during Greed to control downside risk
* Limit trade frequency during high-sentiment periods to avoid overtrading
* Monitor fees closely during active markets, as costs erode returns
* Favor disciplined strategies during Fear for better risk-adjusted performance
* Be cautious of intraday crowding signals during optimistic sentiment

## Project Structure


DS_YOGESWARAN/
├── notebook_1.ipynb        # Full analysis (Google Colab)
├── csv_files/              # Processed datasets
├── outputs/                # Visualizations
├── ds_report.pdf           # Detailed analytical report
└── README.md               # Project overview

## Tools & Technologies

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Google Colab
* GitHub

## How to Review

* View the **Google Colab notebook** for full execution and analysis
* Explore the **outputs folder** for supporting visualizations
* Refer to the **PDF report** for detailed explanations and conclusions

## Notes

This project emphasizes **analytical thinking, data interpretation, and behavioral finance concepts** rather than model building. The focus is on understanding *why* traders behave differently under varying sentiment conditions and how that knowledge can inform better decision-making.
