# Analytics
📊 Trader Behavior vs Market Sentiment Analysis
📌 Project Overview

This project analyzes the relationship between trader performance and Bitcoin market sentiment (Fear & Greed Index).

The goal is to determine:

Does trader performance differ between Fear vs Greed days?

Do traders change behavior based on sentiment?

Which trader segments are more stable across market moods?

🗂 Dataset Description
1️⃣ Historical Trading Data

Contains:

Account

Closed PnL

Trade Size (USD)

Trade Side (Buy/Sell)

Timestamp (IST)

2️⃣ Fear & Greed Index Data

Contains:

Date

Sentiment Classification (Fear / Greed)

Sentiment Value

🧹 Part A — Data Preparation

Steps performed:

Removed duplicate rows

Checked missing values

Converted timestamps (day-first format)

Aggregated data to daily level per account

Merged trading data with sentiment data using date alignment

📊 Key Metrics Created

daily_pnl

win_rate

avg_trade_size

trade_count

long_short_ratio

All datasets were validated after merge to ensure no missing sentiment rows.

📈 Part B — Analysis
🔍 1. Performance Comparison (Fear vs Greed)

Compared:

Average Daily PnL

Win Rate

PnL Volatility (drawdown proxy)

Risk-Adjusted Return

📊 2. Behavioral Changes

Analyzed:

Trade frequency changes

Position size changes

Long/Short bias shifts

👥 3. Segment Analysis

Segments created:

Frequent vs Infrequent Traders

Large vs Small Position Traders

Consistent vs Inconsistent Traders

Each segment was evaluated across sentiment regimes.

💡 Key Insights

1️⃣ Sentiment increases volatility more than skill
Greed days show higher PnL variability without significant improvement in win rate.

2️⃣ Traders increase activity during Greed
Trade frequency and average position size rise during optimistic sentiment periods.

3️⃣ Frequent traders show more stability
High-frequency traders maintain relatively stable performance across sentiment shifts.

🎯 Strategy Recommendations

Implement adaptive risk alerts during high sentiment periods.

Monitor inconsistent traders during Greed phases.

Introduce volatility-based position sizing controls.

⚠️ Limitations

Leverage data was not available in the dataset.

Analysis is performed at daily aggregation level.

Market return was not explicitly controlled.

🔁 Reproducibility

To reproduce:

git clone https://github.com/avinashreddy0/Analytics.git

Then:

Run data cleaning notebook

Generate daily_metrics.csv

Merge with sentiment dataset

Run analysis section

All steps are documented and sequential.

🛠 Tech Stack

Python

Pandas

NumPy

Matplotlib

Seaborn

👨‍💻 Author

Induri Avinash Reddy
B.Tech AIML | Data Analytics Enthusiast