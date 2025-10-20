# 🏀 NBA Shot Selection Evolution (2004–2024)

## 📝 Overview
This repository contains a data science analysis that investigates the profound shift in NBA shot selection and offensive strategy over two decades, comparing the **2003–04 season** (the "mid-range era") with the **2023–24 season** (the "pace-and-space era").

The project utilizes **shot-by-shot logs** to quantify the decline of the mid-range jump shot and the exponential rise of the three-point shot.  
The primary deliverable is a set of comparative visualizations (e.g., **Shot Density Maps**, **Frequency Histograms**) that clearly capture this evolution — often referred to as the **"Three-Point Revolution."**

---

## 📊 Dataset Details

The analysis relies on granular shot log data for the two bookend seasons. The data structure must be consistent to allow for direct comparison between the two decades.

| Feature | 2003–04 Season Data (from `shots.ipynb`) | 2023–24 Season Data (Expected) |
|----------|------------------------------------------|--------------------------------|
| **Source** | Kaggle: `NBA_2004_Shots.csv` (used in `shots.ipynb`) | Expected to be sourced from a comparable data API (e.g., NBA Stats, other public datasets) |
| **Focus** | ≈ 190,000 shot attempts for 2003–04 | All shot attempts for the 2023–24 season |
| **Key Columns** | `SHOT_DISTANCE`, `LOC_X`, `LOC_Y`, `SHOT_MADE`, `SHOT_TYPE` | Equivalent columns are necessary for comparative analysis |

---

### 🔍 Critical Columns for Trend Analysis

The following features enable the core trend analysis:

- **`SHOT_DISTANCE`** – Used to plot the frequency distribution of shots across all ranges (in feet).  
- **`SHOT_TYPE`** – Categorizes attempts as 2-Point or 3-Point attempts.  
- **`SHOT_MADE`** – Used to calculate efficiency metrics like Field Goal Percentage (FG%) and Effective Field Goal Percentage (eFG%) by zone.  
- **`LOC_X` / `LOC_Y`** – Used to generate and compare shot density maps (shot charts).

---

## 🛠️ Setup and Installation

### Dependencies
You must have the following Python libraries installed:

pip install pandas numpy matplotlib seaborn kaggle

## 💡 Data Implications and Analysis Findings

The data analysis reveals a **fundamental change in the geometry and philosophy of NBA offense**, driven by the analytical understanding of **Expected Value (EV)**.

Since a three-point shot is worth **50% more** than a two-point shot, teams have optimized their offense to target only the two most efficient shot locations — **at the rim** and **beyond the arc** — while eliminating the **low-EV mid-range shot**.

---

## 📉 Key Comparative Trends (2004 vs. 2024)

| **Trend** | **2003–04 Season (Baseline)** | **2023–24 Season (Modern Era)** | **Analytical Implication** |
|------------|-------------------------------|----------------------------------|-----------------------------|
| 🏀 **Shot Profile** | *Mid-Range Heavy.* Significant shot volume taken from 10–20 feet. | *Three-and-Rim.* Shots are heavily concentrated at the rim (0–4 ft) and beyond the arc (22+ ft). | **The Death of Mid-Range:** The mid-range jump shot has been deemed analytically inefficient and has been nearly eradicated from high-volume offense. |
| 🎯 **3-Point Attempts** | League average 3PA per game ≈ **15–16 attempts**. | 3PA has approximately doubled or more (≈ **35+ attempts per game**). | **Increased Pace & Value:** The league prioritizes the *Expected Value (EV)* of a shot — with a league-average three-pointer yielding ≈ **1.10 points per attempt**, often higher than a contested mid-range two-pointer. |
| 🔄 **Player Roles** | More defined positional roles (e.g., Centers primarily near the basket). | All players, including Centers and Forwards, are now expected to have 3-point range. | **Positional Fluidity:** The rise of *“positionless basketball”* — every player must be a floor-spacer to maintain offensive efficiency and prevent paint congestion. |

---

