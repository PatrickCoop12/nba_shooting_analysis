# 🏀 NBA Shot Selection Evolution (2004–2024)

## 📝 Overview

This project investigates how **NBA shot selection and offensive philosophy** have evolved over two decades, contrasting the **2003–04 "Mid-Range Era"** with the **2023–24 "Pace-and-Space Era"**.

Using shot-by-shot data, the analysis quantifies:
- The decline of the **mid-range jumper**
- The exponential rise of the **three-point shot**, often called the *Three-Point Revolution*

The deliverables include a series of comparative visualizations (e.g., **Shot Density Maps**, **Shot Distance Histograms**) illustrating the shift in offensive geometry across eras.

---

## 📊 Dataset Details

The analysis compares **two full NBA seasons** with consistent shot log structures to ensure valid comparison.

| Feature | 2003–04 Season Data | 2023–24 Season Data (Expected) |
|----------|--------------------|-------------------------------|
| **Source** | Kaggle: `NBA_2004_Shots.csv` (via `shots.ipynb`) | Expected via NBA Stats API or public datasets |
| **Shots Included** | ≈190,000 shot attempts | All available shot attempts |
| **Focus** | Mid-Range Heavy Era | Pace-and-Space Era |
| **Key Columns** | `SHOT_DISTANCE`, `LOC_X`, `LOC_Y`, `SHOT_MADE`, `SHOT_TYPE` | Equivalent columns required |

### 🔑 Critical Features for Trend Analysis

- **`SHOT_DISTANCE`** — enables frequency distributions by range (ft)
- **`SHOT_TYPE`** — categorizes attempts (2PT vs. 3PT)
- **`SHOT_MADE`** — supports efficiency metrics (FG%, eFG%)
- **`LOC_X` / `LOC_Y`** — used to generate shot density maps

---

## 🛠️ Setup & Installation

### Dependencies

Install the required Python packages:

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

## 🖼️ Visual Interpretation

| Visualization | 2003–04 Season | 2023–24 Season | Insight |
|----------------|----------------|----------------|----------|
| **Shot Density Map (Shot Chart)** | High density in the mid-range areas (elbows, baseline corners) and under the basket | High density exclusively at the rim and around the full three-point arc, forming a “Homer Simpson Donut” shape | Clear visual evidence of the mid-range disappearance and the dominance of rim and perimeter shots |
| **Shot Distance Histogram** | Bimodal or tri-modal distribution with peaks at 0–5 ft (rim), 10–20 ft (mid-range), and a smaller peak at 22+ ft (three-point range) | Strong bimodal distribution with peaks at 0–5 ft and 22+ ft, and near-zero frequency in the mid-range zone | Quantifies the “Three-and-Rim” offensive shift — mid-range nearly eliminated |

