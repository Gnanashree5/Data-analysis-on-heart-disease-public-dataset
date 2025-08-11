# ❤️ Heart Disease Data Analysis & Interactive Dashboards

## 📌 Project Overview
This project analyzes a **Heart Disease Dataset** using **Excel**, **Python**, and **Power BI**, following the *Data Analytics Project Guidesheet* requirements.  
The goal is to:
- Perform **Exploratory Data Analysis (EDA)**
- Build interactive dashboards
- Derive actionable insights about factors affecting heart disease

The project includes **three deliverables**:
1. **EDA & Dashboard in Excel**
2. **EDA & Visualization in Python**
3. **Interactive Power BI Dashboard with DAX**

---

## 📂 Dataset Description
The dataset contains various medical and demographic attributes that help in predicting the presence of heart disease (`target` column).

Below is a **simple explanation of each column** for non-medical readers:

| Column Name  | Meaning | Why It Matters for Heart Disease |
|--------------|---------|-----------------------------------|
| **age** | Patient's age in years | Risk generally increases with age. |
| **sex** | Gender (1 = Male, 0 = Female) | Men often show higher risk earlier in life; patterns differ by gender. |
| **cp** | Chest pain type (0–3) | Some types of chest pain are more strongly linked to heart problems. |
| **trestbps** | Resting blood pressure (mm Hg) | High BP strains the heart and arteries. |
| **chol** | Serum cholesterol (mg/dl) | High cholesterol can lead to artery blockage. |
| **fbs** | Fasting blood sugar > 120 mg/dl (1 = Yes, 0 = No) | High sugar may indicate diabetes, which increases risk. |
| **restecg** | Resting electrocardiogram results | Abnormal ECG can signal heart issues. |
| **thalach** | Maximum heart rate achieved | Lower maximum may suggest limited cardiac function. |
| **exang** | Exercise-induced angina (1 = Yes, 0 = No) | Pain during exercise can be a warning sign. |
| **oldpeak** | ST depression during exercise | Indicates reduced blood flow to the heart. |
| **slope** | Slope of peak exercise ST segment | Used in ECG interpretation for diagnosing heart conditions. |
| **ca** | Number of major vessels (0–3) colored by fluoroscopy | More blocked vessels → higher risk. |
| **thal** | Thalassemia blood disorder status | Certain types relate to higher cardiac risk. |
| **target** | Heart disease presence (1 = Yes, 0 = No) | The outcome we want to analyze and predict. |

---

## 📊 Project Workflow

### **P1: Excel EDA & Dashboard**
**Tasks:**
- Remove duplicates & handle missing values
- Format data types correctly
- Create Pivot Tables & Charts:
  - Heart disease % by age group
  - Heart disease % by gender
  - Cholesterol & BP distributions
- Add Slicers for Age & Gender
- Design a clean, user-friendly dashboard

**Deliverable:** `Heart_Disease_Excel_Dashboard.xlsx`

---

### **P2: Python EDA & Visualization**
**Tasks:**
- Use Pandas for cleaning & preprocessing
- Calculate descriptive statistics
- Create visualizations using Matplotlib & Seaborn:
  - Bar plots, line plots, histograms
  - Box plots for outlier detection
  - Heatmaps for correlations
- Label axes & provide clear titles

**Deliverable:** `heart_disease_analysis.ipynb`

---

### **P3: Power BI Interactive Dashboard**
**Tasks:**
- Import cleaned dataset using Power Query
- Create **Age Group** calculated column for better segmentation
- Build visuals:
  - KPI Cards (Total Patients, % with Disease, Avg Age)
  - Donut chart (Disease distribution)
  - Stacked bar (Gender vs Disease)
  - Ribbon chart (Chest Pain Type by Age Group)
  - Scatter plot (Max HR vs Age colored by Target)
  - Box plot (BP distribution by Target)
- Add Slicers for Age & Gender
- Use DAX for calculated measures like:
```DAX
Total Patients = COUNTROWS('data')
Heart Disease % = DIVIDE(CALCULATE(COUNTROWS(FILTER('data', data[target] = 1))), COUNTROWS('data'))
````

**Deliverable:** `Heart_Disease_Dashboard.pbix`

---

## 📈 Insights from the Analysis

* **Age 50–60** has the highest heart disease prevalence.
* **Males** show slightly higher rates overall, but female rates increase significantly after age 55.
* **High cholesterol** and **low max heart rate** are strongly associated with heart disease.
* **Chest pain type** and **exercise-induced angina** are strong indicators.
* Patients with **more blocked vessels** have much higher risk.

---

## 📂 Repository Structure

```
📁 heart-disease-analysis
 ├── data/
 │   └── heart.csv(2)
 ├── excel/
 │   └── Heart_cleaned_data.xlsx
 ├── python/
 │   └── heart.ipynb
 ├── powerbi/
 │   └── Heart_Disease_Analysis_powerbi.pbix
 ├── README.md
```

---

## 🚀 How to Run

1. **Excel Dashboard**: Open `Heart_Disease_Excel_Dashboard.xlsx` → Use slicers to filter.
2. **Python Notebook**: Run `heart_disease_analysis.ipynb` in Jupyter Notebook or VS Code.
3. **Power BI Dashboard**: Open `Heart_Disease_Dashboard.pbix` in Power BI Desktop.


---

## 🏆 Purpose

This project demonstrates:

* End-to-end data analysis workflow
* Ability to present insights visually
* Skills in Excel, Python, and Power BI
* Understanding of medical dataset interpretation

```
