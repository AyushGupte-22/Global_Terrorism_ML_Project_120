# 🌍 Global Terrorism ML Project

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Status](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-Academic-green)

## 📖 Project Overview

This repository presents a **comprehensive Exploratory Data Analysis (EDA)** of the [Global Terrorism Database](https://www.start.umd.edu/data-tools/gtd), covering **289,796 incidents worldwide (1970–2020)**. The project focuses on **data cleaning, temporal and spatial terrorism pattern analysis**, and sets the foundation for **predictive modeling** to attribute incidents to terrorist groups.

This project was developed by **Ayush Gupte (PRN: 22070521120, Batch 2022–26)** as part of an academic Machine Learning module.

---

## 📊 Dataset Description

- **Source:** [GTD](https://www.start.umd.edu/data-tools/gtd)  
- **Timeframe:** 1970–2020  
- **Records:** 289,796  
- **Original Features:** 135 → **Reduced to 11 (model-ready)**  
- **Target Variable:** `GroupName` (responsible terrorist group)  

**Final Selected Columns:**  
`Year`, `Month`, `Country`, `Region`, `Latitude`, `Longitude`, `AttackType`, `TargetType`, `WeaponType`, `Suicide`, `GroupName`

---

## 🔍 EDA Methodology

The EDA (in `Main_EDA_3.ipynb`) explores **univariate, bivariate, and multivariate** relationships to uncover key patterns.

### **1. Temporal Analysis**
- Year-wise incident trend (**1970–2020**):  
  ![Yearly Incidents](Global_Terrorism_Incident_Map.png)
- **Insight:** Sharp rise in incidents post-2000, **peak in 2014** (ISIL surge).

### **2. Geographical Hotspots**
- **Top 10 affected countries:** Iraq, Pakistan, Afghanistan lead.
- **Heatmaps by region and attack type** reveal dominant methods across continents.

### **3. Attack & Group Profiling**
- **Most common attack type:** **Bombings/Explosions** (twice as frequent as Armed Assaults).  
- **Suicide Attacks:** <5% of total but highly impactful.  
- **Top Groups:** **Taliban & ISIL** dominate post-2010.

### **4. Interactive Visualizations**
- **Geospatial map:** Explore incidents by location (HTML map in repo: `global_terrorism_map.html`).

---

## 🧹 Data Cleaning Pipeline

Implemented in `Data_Cleaning_2.ipynb`:

1. **Dropped irrelevant & high-missing (>20%) columns**.  
2. **Selected 10 features + target** for modeling relevance.  
3. **Imputation:**  
   - Mean for numerical (`Latitude`, `Longitude`).  
   - Mode for categorical (`AttackType`, `WeaponType`).  
4. **Standardized naming** (`Unknown` → `Unknown_Group`).  
5. **Saved final dataset:** `globalterrorismdb_cleaned.csv`.

---


## 📂 Project Structure

```
├── Cleaned Dataset/                # Cleaned GTD dataset
├── Original Dataset/               # Raw GTD dataset
├── Data_Cleaning_2.ipynb           # Data preprocessing
├── Main_EDA_3.ipynb                # EDA & insights
├── Global_Terrorism_Incident_Map.png  # Map visualization
├── global_terrorism_map.html       # Interactive map
├── ML Report.docx                  # Detailed project report
└── README.md                       # Project documentation
```

---

## 🚀 Future Enhancements

- **Model Development:** Implement & tune **Random Forest, XGBoost, and Neural Networks** for group prediction.  
- **Feature Engineering:** Add derived variables (e.g., geospatial clusters, temporal seasonality).  
- **Deployment:** Build an interactive **Streamlit/Dash** dashboard for real-time insights.  
- **Model Explainability:** Integrate **SHAP values** for understanding ML decisions.

---

## 🎯 Key Insights

- **2014:** Peak in terrorism due to ISIL.  
- **Geographical Hotspots:** Middle East & South Asia dominate post-2000.  
- **Tactics:** **Bombings** remain the most common method.  
- **Groups:** Taliban & ISIL lead in recent decades.  
- **Suicide Attacks:** Rare but disproportionately impactful.

---

## ⚙️ Setup Instructions

### **1. Clone Repository**
```bash
git clone https://github.com/AyushGupte-22/Global_Terrorism_ML_Project_120.git
cd Global_Terrorism_ML_Project_120
```

## 👤 Author

**Ayush Gupte**  
PRN: 22070521120 | Batch: 2022–26 | Section: C  
GitHub: [AyushGupte-22](https://github.com/AyushGupte-22)

---

## 📜 License
This project is for **academic & research purposes only**.  
Data is sourced from [GTD](https://www.start.umd.edu/data-tools/gtd).

---
