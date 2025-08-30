# Trading-Sentiment-Analysis
This repository contains all the files related to the Project/Assignment about exploring and analyzing all the details like behaviour and market trend using two given datasets.

# Analysis of Trader Behavior vs. Market Sentiment

This project conducts an in-depth analysis of the relationship between cryptocurrency trader behavior and overall market sentiment, as measured by the popular Fear & Greed Index. By merging historical trade data with daily sentiment scores, this analysis reveals a complex and fascinating pattern.


The complete analysis can be found in the Jupyter Notebook located at `notebooks/notebook_1.ipynb`.

![Bitcoin Fear & Greed Index Over Time](https://raw.githubusercontent.com/Rohit-03-19/ds_Rohit-Parida/main/output/Bitcoin%20Fear%20&%20Greed%20Index%20Over%20Time.png)

---

## 🎯 Objective

The primary goal of this project is to explore how key trading metrics—such as **profitability, volume, and risk-taking**—align or diverge from the prevailing market sentiment. The analysis aims to identify hidden trends and data-driven signals that can inform smarter, more strategic trading decisions.

---

## 📂 Datasets

This analysis utilizes two primary data sources:

1.  **Bitcoin Market Sentiment:** A time-series dataset of the daily Fear & Greed Index.
    * **Shape:** 2644 rows, 4 columns
2.  **Historical Trader Data:** Transactional trade data from a high-volume platform.
    * **Shape:** 211224 rows, 16 columns

---

## 🛠️ Methodology

The project follows a structured data analysis workflow:

1.  **Data Cleaning & Preprocessing:** Both datasets were loaded, cleaned, and formatted. Timestamps were standardized, and sentiment classifications were consolidated.
2.  **Data Merging:** The transactional trade data was merged with the daily sentiment data to associate each trade with the market sentiment on that specific day.
3.  **Feature Engineering:** New features were created to facilitate analysis, including `outcome` (Win/Loss) and `Size USD`.
4.  **Exploratory Data Analysis (EDA):** A comprehensive EDA was performed to compare trader metrics across the different sentiment categories.
5.  **Conclusion & Strategy Formulation:** The insights from the EDA were synthesized into a final conclusion and a set of actionable trading strategies.

---

## 📊 Key Findings

The analysis uncovered a nuanced relationship where different sentiment periods offered distinct trading characteristics.

#### **Finding 1: 'Fear' Drives Total Profit, but 'Greed' Yields Higher Average Profit Per Trade**
The data shows a split in how profitability is achieved across different sentiments.

* **Total Cumulative PnL:** The 'Fear' sentiment generated the highest total profit.
* **Win/Loss Ratio:** The proportion of winning trades was highest during 'Fear'.
* **Average PnL:** However, the average profit *per trade* was highest during 'Greed'.

**Interpretation:** While the 'Fear' period generated the most overall profit due to high activity and a solid win rate, individual trades made during 'Greed' were more potent and lucrative on average.

![Total Cumulative PnL by Market Sentiment](https://raw.githubusercontent.com/Rohit-03-19/ds_Rohit-Parida/main/output/Total%20Cumulative%20PnL%20by%20Market%20Sentiment.png)

![Average Trader PnL by Market Sentiment](https://raw.githubusercontent.com/Rohit-03-19/ds_Rohit-Parida/main/output/Average%20Trader%20PnL%20by%20Market%20Sentiment.png)

![Proportion of Trade Outcomes by Market Sentiment](https://raw.githubusercontent.com/Rohit-03-19/ds_Rohit-Parida/main/output/Proportion%20of%20Trade%20Outcomes%20by%20Market%20Sentiment.png)

#### **Finding 2: Market 'Fear' Drives the Highest Trading Activity**
Contrary to the common belief that greed drives market participation, this dataset shows that fear was the primary driver of trading activity.

* **Trade Frequency:** The number of trades was overwhelmingly highest during periods of 'Fear'.
* **Total Volume:** Similarly, the total dollar volume traded was more than four times higher during 'Fear' than during 'Greed'.

**Interpretation:** This suggests that market panic and uncertainty trigger significantly more activity than market euphoria. Traders in this dataset were most active during downturns.

![Trade Frequency by Market Sentiment](https://raw.githubusercontent.com/Rohit-03-19/ds_Rohit-Parida/main/output/Trade%20Frequency%20by%20Market%20Sentiment.png)

![Total Trading Volume by Market Sentiment](https://raw.githubusercontent.com/Rohit-03-19/ds_Rohit-Parida/main/output/Total%20Trading%20Volume%20by%20Market%20Sentiment.png)

#### **Finding 3: Risk-Taking Is Highest During 'Fear'**
Traders were willing to place their biggest bets when the market was fearful, a strategy that correlated with the highest total profits.

* **Average Position Size:** The average trade size was largest during periods of 'Fear', exceeding $5,000.

**Interpretation:** The combination of high average position sizes and the highest total profitability during 'Fear' suggests that traders were making calculated, high-conviction moves during periods of pessimism, which paid off in aggregate.

![Average Position Size by Market Sentiment](https://raw.githubusercontent.com/Rohit-03-19/ds_Rohit-Parida/main/output/Average%20Position%20Size%20by%20Market%20Sentiment.png)

---

## 💡 Actionable Strategies & Conclusion

Based on this analysis, the optimal trading strategy appears to depend on a trader's style.

1.  **Strategy for High-Frequency/Consistent Gains:** The 'Fear' period is best suited for this approach due to the high number of trades and the favorable win/loss ratio.
2.  **Strategy for High-Impact/"Home Run" Trades:** The 'Greed' period, while less active, offered the highest average profit per trade, suggesting a strategy of making fewer, more selective trades.
3.  **Use Activity as an Indicator:** High trade **frequency** during 'Fear' is a sign of a highly active and profitable market. In contrast, low frequency during 'Greed' indicates a more selective, high-stakes environment.

In conclusion, the data reveals a dual-sided market. **'Fear' is the engine of activity and consistent profit**, rewarding those who participate frequently. **'Greed' is the realm of selective, high-reward trades**, favoring patience over volume.

---
The raw data is located in the `csv_files/` directory, and all chart outputs are saved in the `output/` directory.
