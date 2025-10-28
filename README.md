# Stack and Roll Hedge (WTI Futures)

This project analyzes and backtests **Stack-and-Roll hedging strategies** for West Texas Intermediate (WTI) crude oil futures. It compares monthly versus quarterly rollover methods to evaluate firm value stability, margin requirements, and profit & loss performance under real-world price dynamics from **2016–2022**.

---

## Overview
The study models a Texas oil producer hedging 100,000 barrels per month over five years, using CME-standard futures contracts.  
Two hedging schemes are simulated:
1. **Monthly Hedge:** Rolling into the 3rd-nearby contract each month.  
2. **Quarterly Hedge:** 3:2:1 stacked rollover every quarter.

Performance metrics include:
- Daily and cumulative P&L  
- Margin balance and cash balance  
- Firm value trajectory  
- Minimum, maximum, and terminal firm value  

---

## Key Findings
- The **quarterly stack** outperformed the monthly hedge across most of the 2016–2022 period.  
- During prolonged backwardation (e.g., post-COVID and 2021–2022 energy shocks), quarterly hedging captured **higher roll yield** due to multi-leg exposure.  
- Monthly hedging provided smoother cash flow but missed convergence gains from shorter maturities.  
- Transaction costs and basis risk sensitivity were also discussed, highlighting **regime-dependent hedging effectiveness**.

---

## Tools & Code
Developed in **R** using:
- `dplyr`, `tidyr`, `purrr`, `ggplot2`, `stringr`, and `readxl` packages.

The full R script (Appendix) demonstrates:
- Data cleaning and reshaping of historical futures prices  
- Roll schedule generation  
- Margin call and cash flow simulation logic  
- Visualization of firm value and cumulative P&L

---

## 📈 Reference Concepts
- Johnson (1960), *The Theory of Hedging and Speculation in Commodity Futures*  
- Ederington (1979), *The Hedging Performance of the New Futures Markets*  
- Hull (2018), *Options, Futures, and Other Derivatives*  
- Bianchi et al. (2016), *Roll Strategy Efficiency in Commodity Futures Markets*  

---

## 📬 Author
**Levin Curt David**  
Rice University — STAT 449: Quantitative Financial Risk Management
Instructor: Dr. Katherine Ensor, Dr. Wentao Zhao, Arnold Muchatibaya  

---

> *This repository is for academic and illustrative purposes only and does not represent financial advice or trading recommendations.*
