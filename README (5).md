# 🌾 Seasonal Agriculture Performance Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-EDA-150458.svg)
![Status](https://img.shields.io/badge/status-complete-brightgreen.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Internship](https://img.shields.io/badge/Internship%20Project-VOIS%20×%20AICTE-e60000.svg)

> 🎓 **Major Project — VOIS & Vodafone Idea Foundation Data Analytics Internship** (AICTE + Edunet Foundation, Batch 1, 2026–27)

## 📖 Overview

A data analytics project investigating how agricultural performance — yield, profitability, resource efficiency — varies across India's three growing seasons (**Kharif, Rabi, Zaid**). Built as the Major Project for the **VOIS & Vodafone Idea Foundation Data Analytics Internship** (AICTE + Edunet Foundation, Batch 1, 2026–27).

## ❓ Problem Statement

Agricultural performance is shaped by seasonal variation in environmental conditions, farming practices, resource availability and market conditions — but raw data alone doesn't explain how or why. This project analyzes 4,000 farm-level records to surface meaningful seasonal patterns, relationships and evidence-based recommendations for agricultural planning.

## 📊 Dataset

| | |
|---|---|
| Records | 4,000 farms |
| Features | 28 (environmental, resource, economic) |
| Seasons | Kharif, Rabi, Zaid |
| Crops | 8 — Wheat, Rice, Maize, Cotton, Pulses, Chilli, Groundnut, Sugarcane |
| States | 8 |
| Irrigation methods | 4 — Drip, Flood, Sprinkler, Rainfed |

## 🔍 Methodology

1. **Data cleaning** — season/crop-wise median imputation for missing values, duplicate checks
2. **Descriptive & statistical analysis** — summary statistics, skewness
3. **Outlier investigation** — IQR method, analyzed within crop groups
4. **Univariate, bivariate & multivariate analysis**
5. **Correlation analysis** — full numeric correlation matrix
6. **Seasonal comparison** — with Kruskal-Wallis significance testing
7. **Three original analyses** — profitability deep-dive, irrigation economic efficiency (engineered profit-per-water metric), and crop segmentation (engineered revenue-to-cost ratio)

## 💡 Key Findings

- **Kharif is the strongest season, Zaid the weakest.** Kharif posts the highest yield and profit and the lowest loss rate; Zaid is the only season with a *negative* average profit and a 64.5% loss rate — a difference confirmed statistically significant (Kruskal-Wallis, p < 0.05), not random noise.
- **Close to half of all farms are loss-making overall.** Wheat (74.1% loss rate), Rice (66.4%) and Maize (63.7%) are loss-making in the *majority* of records — a structural issue, not a seasonal one — while Chilli (18.0% loss rate) and Sugarcane stay consistently profitable.
- **No agronomic input correlates meaningfully with yield.** Rainfall, soil NPK, soil pH and fertilizer all show |r| < 0.06 with yield — crop choice and season explain far more of the variation than input variables do.
- **Drip irrigation wins on every front** — yield, water use, and profit generated per unit of water — simultaneously.
- **Yield "outliers" are a scale artifact, not errors.** 97% of flagged outliers are simply Sugarcane records, whose yield is naturally measured on a ~15–20x larger scale than other crops.

📓 Full analysis, code and all visualizations: [`Seasonal_Agriculture_Performance_Analysis.ipynb`](./Seasonal_Agriculture_Performance_Analysis.ipynb)

## 🛠️ Tech Stack

Python · Pandas · NumPy · Matplotlib · Seaborn · SciPy · Google Colab

## 📂 Repository Structure

```
├── Seasonal_Agriculture_Performance_Analysis.ipynb   # Full analysis notebook
├── seasonal_agriculture_performance_dataset.csv       # Dataset
├── README.md
└── LICENSE
```

## 🚀 How to Run

1. Clone or download this repository
2. Open `Seasonal_Agriculture_Performance_Analysis.ipynb` in [Google Colab](https://colab.research.google.com/)
3. Upload `seasonal_agriculture_performance_dataset.csv` to the Colab session (Files pane → Upload)
4. Runtime → Run all

## 🔮 Future Scope

- Incorporate multi-year data to study long-term seasonal trends
- Add a detailed cost breakdown (labor, seed, fertilizer, irrigation)
- Build a predictive ML model for yield/profit estimation
- Validate findings against real geographic/climate data
- Develop a simple farmer-facing dashboard

## 🎓 Acknowledgments

Built as part of the **VOIS & Vodafone Idea Foundation Data Analytics Internship**, delivered in partnership with **AICTE** and **Edunet Foundation**.

## 👤 Author

**Kashish Arya**
B.Tech CSE (AI/ML) · Vidya College of Engineering
[GitHub](https://github.com/Kashish7714) · [LinkedIn](https://linkedin.com/in/kashish-arya-062249383)

## 📄 License

This project is licensed under the MIT License — see [LICENSE](./LICENSE) for details.
