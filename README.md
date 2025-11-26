# Junior Data Scientist Assignment: Trader Behavior Insights

## Overview
This project was completed as an assignment for the Junior Data Scientist role, focusing on analyzing the relationship between cryptocurrency market sentiment and active trader performance. The core objective was to uncover strategic insights and hidden patterns within high-frequency trade data that can inform smarter Web3 trading strategies.

---

##  Project Objective
To explore and quantify the relationship between market sentiment, as measured by the Fear & Greed Index, and the financial performance (`Closed PnL`) and trading behavior of participants on the Hyperliquid platform.

##  Data Sources

Two primary datasets were utilized for this analysis:

1.  **Historical Trader Data (Hyperliquid):** Detailed, high-frequency records of individual trades, including `account` ID, `symbol`, `execution price`, `size`, `side`, `time`, and most importantly, `closedPnL`.
2.  **Bitcoin Market Sentiment Data (Fear & Greed Index):** Daily time-series data providing the `Classification` (e.g., Fear, Greed, Neutral) and the underlying sentiment `score`.

##  Methodology & Analysis

The analysis was performed in a structured three-step process:

### 1. Data Merging & Preparation
* Both datasets were loaded, cleaned for consistency, and standardized.
* The high-frequency trade data was merged with the daily sentiment data by aligning the trade timestamp with the appropriate day's sentiment score, allowing for direct comparison of performance under different market conditions.

### 2. Feature Engineering
Key features were engineered to provide deeper analytical depth, including:
* **Time-Series Features:** Trade time of day, day of week.
* **Account-Specific Metrics:** Cumulative trade count and volume per account (to identify "whales").
* **Categorical Buckets:** Classification of trades into `trade_size_bucket` (Small, Medium, Large) and PnL into `pnl_bucket` (Win, Loss, Neutral).
* **Market Risk:** Calculation of coin-specific volatility.

### 3. Exploratory Data Analysis (EDA) & Visualization
* Visualizations (histograms, box plots, scatter plots) were generated to illustrate the distribution of PnL, trade volume by sentiment, and performance differences across various cryptocurrency symbols.
* The primary focus was placed on identifying **non-linear relationships** and **extreme outliers** to explain the market's risk-reward dynamics.

---

##  Deliverables

This repository contains the full set of artifacts used for the assignment submission:

| File Name | Description |
| :--- | :--- |
| `marketanalysis.ipynb` | The complete Jupyter Notebook containing all Python code for data loading, cleaning, feature engineering, statistical analysis, and visualization generation. |
| `insight.docx` | A professional document detailing the full strategic insights, conclusions, and hidden patterns discovered from the dataset. |


##  Conclusion

The analysis successfully established a clear link between trader behavior (high activity during fear) and asset choice (high-risk altcoins) and the resulting high-variance PnL profile. The strategic insights derived are detailed in the accompanying report.

---

