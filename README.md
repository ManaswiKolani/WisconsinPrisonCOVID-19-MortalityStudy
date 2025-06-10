<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExN203bno5dTVwZGZ5N3F6NnNoOThmZ3hkamZqMjJqOG52b2pnY3U5NSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Qu1fT51CG14ksIkASL/giphy.gif" width="150" alt="AI thinking gif" />

# 🏛️🦠 Wisconsin Prison COVID-19 Mortality Study 


A concise analysis and codebase showing that the share of COVID-19 deaths among Wisconsin inmates differs significantly from the national prison population.

---

## Overview 🔍  
This project asks **“Did Wisconsin prisons experience a different COVID-19 mortality rate than U.S. prisons overall?”** Using *New York Times* facility-level data (Mar 2020 – Mar 2021) we:

1. 📊 Aggregate inmate populations and deaths to the state level  
2. 🧮 Estimate mortality proportions for Wisconsin and the entire U.S.  
3. ⚖️ Run a two-sample difference-in-proportions test via 10 000-iteration Monte Carlo simulation  
4. 🖼️ Visualize results with normal-curve and scatter-plot graphics  

## Data 💾  
| Field | Description |
|-------|-------------|
| `facility_state` | Two-letter state / territory code |
| `max_inmate_population_2020` | Peak population between Mar 2020 – Mar 2021 |
| `total_inmate_deaths` | Cumulative confirmed COVID-19 inmate deaths |

*Dataset:* **`facilities.csv`** compiled by *The New York Times*.

## Key Numbers 📊  
| Metric | Wisconsin | United States |
|--------|-----------|---------------|
| Inmates analysed | 21 645 | 1 063 866 |
| COVID-19 deaths | 13 | 3 986 |
| Mortality proportion | 0.060 % | 0.375 % |

*Test statistic:* 0.0006  
*p-value:* **0.038** (α = 0.05) → reject H₀; proportions differ.

## Reproduce the Analysis 🛠️  
```r
# 1. Install packages
install.packages(c("tidyverse", "ggplot2"))

# 2. Run the pipeline
source("analysis.R")  # outputs tables & figures to /outputs
