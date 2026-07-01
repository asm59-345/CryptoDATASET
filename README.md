# Hyperliquid Trader Performance vs. Market Sentiment Analysis

This repository contains an end-to-end data analytics solution designed for the **Primetrade.ai** Data Science hiring assignment. The project explores the quantitative relationship between trader behavior (historical trade performance data from Hyperliquid) and broad crypto market sentiment (Bitcoin Fear and Greed Index).

---

##  Project Objective
The core goal of this analysis is to:
1. **Merge & Preprocess** large-scale decentralized exchange trading data with daily cryptographic market sentiment indicators.
2. **Uncover Hidden Patterns** regarding risk tolerance, capital efficiency, and trading bias across different psychological market phases.
3. **Formulate Smarter Trading Strategies** based on empirical win-rates, trade sizes, and directional biases.

---

##  Key Findings & Market Insights

Our analysis processed **211,218 unique matched historical trades** across 5 sentiment tiers (*Extreme Fear, Fear, Neutral, Greed, Extreme Greed*). 

### 1. The "Fear" Paradox (High-Conviction Volume)
* While retail sentiment drops during the **Fear** phase, professional traders on Hyperliquid scale their average position sizes to the absolute peak of **$7,816.11**.
* This phase generates the highest cumulative profitability across the entire dataset (**$3.35M+ Total PnL**), proving that professional capital treats "Fear" as a primary liquidity window.

### 2. "Extreme Greed" Strategic Capital Preservation
* Paradoxically, **Extreme Greed** features the highest nominal win-rate (~89.17%), but the lowest average trade size (**$3,112.25**). 
* Data shows a sharp pivot toward **SELL/Short orders (55.14%)** during Extreme Greed, indicating that advanced traders systematically risk-off and scale into hedges or contrarian reversals when the crowd is euphoric.

### 3. Structural Metrics Table
| Market Sentiment | Total Trades | Average Size (USD) | Total Profit/Loss (PnL) | Win Rate (%) | Major Order Bias |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Extreme Fear** | 21,400 | \$5,349.73 | \$739,110.22 | 76.22% | BUY (51.10%) |
| **Fear** | 61,837 | \$7,816.11 | \$3,357,155.19 | 87.29% | SELL (51.05%) |
| **Neutral** | 37,686 | \$4,782.73 | \$1,292,921.28 | 82.39% | BUY (50.33%) |
| **Greed** | 50,303 | \$5,736.88 | \$2,150,129.28 | 76.89% | SELL (51.14%) |
| **Extreme Greed** | 39,992 | \$3,112.25 | \$2,715,170.62 | 89.17% | **SELL (55.14%)** |

---

##  Tech Stack & Library Frameworks
* **Language:** Python 3.x
* **Data Wrangling:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Environment:** Google Colab / Jupyter Notebooks

---

##  How to Execute the Script (Google Colab / Local Machine)

### Option A: Google Colab Setup (Recommended)
1. Go to [Google Colab](https://colab.research.google.com/).
2. Open a new notebook and create a code cell.
3. Upload `historical_data.csv` and `fear_greed_index.csv` using the file explorer icon on the left sidebar.
4. Copy-paste the provided analysis script into the cell and run it.

### Option B: Local Environment Execution
1. Clone this repository or download the script file.
2. Install the necessary dependencies via your terminal:
   ```bash
   pip install pandas numpy matplotlib seaborn
