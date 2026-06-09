# PowerLens — Household Energy Consumption Analysis

> **KaynorData** · Descriptive Analytics · Energy Domain

Lentille d'analyse sur la consommation électrique

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange)

---

## 📌 Project Overview

**PowerLens** is a descriptive analytics project focused on understanding **residential electricity consumption patterns** using real-world household data.

This project answers the fundamental question:

> *"What happened with household electricity consumption over time — and when, how much, and why does it vary?"*

Inspired by real operational challenges at  **CIE (Compagnie Ivoirienne d'Électricité)** , this project demonstrates how raw energy data can be transformed into actionable insights for utility companies, energy auditors, and smart grid operators.

---

## 🎯 Business Questions Answered

| # | Question                                                    | Type       |
| - | ----------------------------------------------------------- | ---------- |
| 1 | What is the overall distribution of global active power?    | Univariate |
| 2 | Which hours of the day show peak consumption?               | Temporal   |
| 3 | Which days of the week are the most energy-intensive?       | Temporal   |
| 4 | How does monthly and yearly consumption evolve?             | Trend      |
| 5 | What is the relationship between active and reactive power? | Bivariate  |
| 6 | Are there consumption spikes or anomalous periods?          | Pattern    |

---

## 📁 Project Structure

```
powerlens/
├── data/
│   └── .gitkeep                    # Dataset excluded — see Data Source below
├── notebooks/
│   ├── 01_data_loading.ipynb       # Data ingestion & quality check
│   ├── 02_eda_univariate.ipynb     # Distribution analysis
│   ├── 03_eda_bivariate.ipynb      # Correlations & relationships
│   └── 04_visualisations.ipynb     # Final charts & dashboard-ready figures
├── reports/
│   └── figures/                    # Exported charts (PNG/SVG)
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

---

## 📊 Dataset

**Source:** [UCI Machine Learning Repository — Individual Household Electric Power Consumption](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption)

| Attribute | Detail                                     |
| --------- | ------------------------------------------ |
| Period    | December 2006 – November 2010 (47 months) |
| Frequency | 1-minute intervals                         |
| Records   | ~2 million rows                            |
| Size      | ~124 MB                                    |

**Key variables used:**

| Variable                  | Description                     | Unit           |
| ------------------------- | ------------------------------- | -------------- |
| `Global_active_power`   | Total household active power    | kilowatt (kW)  |
| `Global_reactive_power` | Total household reactive power  | kilowatt (kW)  |
| `Voltage`               | Average voltage                 | volt (V)       |
| `Global_intensity`      | Average current intensity       | ampere (A)     |
| `Sub_metering_1`        | Kitchen appliances              | watt-hour (Wh) |
| `Sub_metering_2`        | Laundry room                    | watt-hour (Wh) |
| `Sub_metering_3`        | Water heater & air conditioning | watt-hour (Wh) |

> ⚠️ The dataset file exceeds GitHub's 100 MB limit and is excluded from this repository.
> Download it directly from the UCI link above and place it in the `data/` folder.

---

## 🔍 Key Findings

> *(To be updated as analysis progresses)*

* 📈 **Peak hours:** Consumption peaks observed between **17h–21h** on weekdays
* 📅 **Seasonal trend:** Higher consumption in winter months (Dec–Feb)
* ⚡ **Sub-metering:** Sub-metering 3 (water heater/AC) accounts for the largest share of consumption
* 🔗 **Correlation:** Strong positive correlation between `Global_active_power` and `Global_intensity`

---

## 🛠️ Tech Stack

| Tool             | Purpose               |
| ---------------- | --------------------- |
| Python 3.10+     | Core language         |
| Pandas           | Data manipulation     |
| Matplotlib       | Static visualizations |
| Seaborn          | Statistical plots     |
| NumPy            | Numerical operations  |
| Jupyter Notebook | Interactive analysis  |

---

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone git@github-kaynordata:Kaynor-Data/powerlens.git
cd powerlens

# 2. Create a virtual environment
python -m venv venv
source venv/bin/activate        # Linux/Mac
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Download the dataset
# Place household_power_consumption.txt in data/

# 5. Launch Jupyter
jupyter notebook
```

---

## 📈 Notebooks Guide

| Notebook              | Description                                           | Duration |
| --------------------- | ----------------------------------------------------- | -------- |
| `01_data_loading`   | Load data, handle missing values, parse datetime      | ~15 min  |
| `02_eda_univariate` | Histograms, boxplots, summary statistics per variable | ~20 min  |
| `03_eda_bivariate`  | Correlation matrix, scatter plots, heatmaps           | ~20 min  |
| `04_visualisations` | Hourly/daily/monthly trends, export-ready charts      | ~25 min  |

---

## 🧭 Project Roadmap

This project is **Part 1 of 4** in the KaynorData Energy Analytics Series:

| Project              | Focus                            | Status         |
| -------------------- | -------------------------------- | -------------- |
| **PowerLens**  | Descriptive — What happened?    | 🔄 In Progress |
| **WattScope**  | Diagnostic — Why did it happen? | ⏳ Planned     |
| **GridPulse**  | Predictive — What will happen?  | ⏳ Planned     |
| **EnergyFlow** | Prescriptive — How to optimize? | ⏳ Planned     |

---

## 👤 Author

**Beh Konaté**
Data Analyst · KaynorData
📧 konatebeh21@gmail.com
🔗 [GitHub @Kaynor-Data](https://github.com/Kaynor-Data)
📺 [YouTube @KaynorData](https://youtube.com/@KaynorData)

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](https://claude.ai/chat/LICENSE) file for details.

---

*Built with ❤️ by KaynorData — Turning raw data into clear insights.*
