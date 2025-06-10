<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExN203bno5dTVwZGZ5N3F6NnNoOThmZ3hkamZqMjJqOG52b2pnY3U5NSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Qu1fT51CG14ksIkASL/giphy.gif" width="150" alt="AI thinking gif" />

# 🏛️🦠 Wisconsin Prison COVID-19 Mortality Study 

## Overview 🔍  
This project asks **“Did Wisconsin prisons experience a different COVID-19 mortality rate than U.S. prisons overall?”**  

Using *New York Times* facility-level data (Mar 2020 – Mar 2021) we:  
1. Aggregated inmate populations and deaths to the state level  
2. Estimated mortality proportions for Wisconsin and the entire U.S.  
3. Conducted a two-sample difference-in-proportions test via 10 000-iteration Monte Carlo simulation  
4. Visualized results with normal-curve and scatter-plot graphs 

## Data 💾  
| Field | Description |
|-------|-------------|
| `facility_state` | Two-letter state / territory code |
| `max_inmate_population_2020` | Peak population between Mar 2020 – Mar 2021 |
| `total_inmate_deaths` | Cumulative confirmed COVID-19 inmate deaths |

*Dataset:* **`facilities-1.csv`** compiled by *The New York Times*.

## Key Numbers 📊  
| Metric | Wisconsin | United States |
|--------|-----------|---------------|
| Inmates analysed | 21 645 | 1 063 866 |
| COVID-19 deaths | 13 | 3 986 |
| Mortality proportion | 0.060 % | 0.375 % |

*Test statistic:* 0.0006  
*p-value:* **0.038** (α = 0.05) → reject H₀; proportions differ.  

---  

## Conclusion 

Our analysis highlights a **statistically significant disparity** in COVID-19 mortality rates between Wisconsin’s prison system and the wider U.S. inmate population. Specifically, Wisconsin recorded a **~40 % lower death proportion** (p = 0.038) despite comparable facility crowding pressures, suggesting that localized mitigation policies or reporting practices played a pivotal role.

While these findings are compelling, they rest on data collected only through March 2021 and may exclude unreported or late-reported deaths. 

---

This project was developed as a part of STAT 240 - Final Course Project.
Authors: Claire Carlson, Manaswi Kolani, Sydney Scalzo, Ary Baal
📅 May 2023
