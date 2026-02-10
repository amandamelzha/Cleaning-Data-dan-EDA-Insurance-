# 🏥 Healthcare Cost Analysis Dashboard (Tableau)

## 📌 Project Overview
This project analyzes **healthcare costs** to identify **key drivers of high medical expenses** using **data visualization and business intelligence** with **Tableau**.

The analysis focuses on:
- Understanding the distribution of healthcare costs
- Identifying **high-cost patients**
- Exploring major risk factors such as **smoking behavior, age, and BMI**
- Providing **data-driven recommendations** for cost management

---

## 📂 Dataset
The dataset contains patient-level healthcare information with the following variables:

- `age`
- `sex`
- `bmi`
- `children`
- `smoker`
- `region`
- `charges` (medical cost)

**Total records:** 1,337 patients

---

## 🧹 Data Cleaning & Preparation
Data preparation was performed directly in **Tableau** to ensure the dataset was ready for analysis and visualization.

### Data Quality Checks
- No significant missing values
- No duplicate records
- Numerical values fall within reasonable ranges

### Data Type Adjustment
- **Measures:** Age, BMI, Charges  
- **Dimensions:** Sex, Smoker, Region, Children  

---

## 🔄 Data Transformation

### 🔹 Age Group
Age was grouped into:
- `<30`
- `30–45`
- `46–64`

**Reason:**  
Healthcare costs do not increase linearly by age but tend to rise at specific life stages.

---

### 🔹 BMI Category
BMI values were categorized as:
- Underweight
- Ideal
- Overweight
- Obese

**Reason:**  
BMI categories are more meaningful for healthcare risk analysis than raw BMI values.

---

### 🔹 Cost Category (Percentile-based)
Healthcare costs were segmented using percentiles:
- **Low Cost:** Bottom 10%
- **Normal Cost:** Middle 80%
- **High Cost:** Top 10%

**Reason:**  
Cost distribution is highly right-skewed, making percentile-based segmentation more robust than fixed thresholds.

---

## 🧮 Calculated Fields
The following calculated fields were created in Tableau:
- Age Group
- BMI Category
- Cost Category
- High Cost Patient Ratio (%)

---

## 📊 Exploratory Data Analysis (EDA)

### Dashboard 1 — Healthcare Cost Overview
**Purpose:** Provide a high-level overview of healthcare costs.

**Visualizations:**
- KPI Cards (Total Cost, Average Cost, High Cost Ratio)
- Cost Distribution Histogram
- Cost Category Pie Chart
- Smoker vs Non-Smoker Cost Comparison

**Key Findings:**
- Healthcare costs are not evenly distributed
- Approximately **10% of patients fall into the High Cost category**
- Smokers incur significantly higher medical costs than non-smokers

---

### Dashboard 2 — Risk & Impact Analysis
**Purpose:** Identify high-risk patient segments.

**Visualizations:**
- Scatter Plot (Age vs Charges)
- Average Charges by Age Group
- Average Charges by BMI Category
- Risk Heatmap (Age Group × BMI Category)

**Key Findings:**
- Medical costs increase with age
- Obese patients have the highest average costs
- The combination of older age and high BMI represents the highest cost risk

---

## 💡 Key Insights
- Healthcare costs are **highly skewed**, with a small group driving most expenses
- **Smoking behavior** is the most dominant cost driver
- Risk increases further when smoking is combined with **older age** and **high BMI**
- Gender, region, and number of children show relatively minor impact on cost variation

---

## ✅ Recommendations
Based on the analysis:
- Prioritize preventive healthcare programs targeting **smokers**
- Promote weight management and healthy lifestyle initiatives
- Apply preventive monitoring for high-risk age groups
- Adopt **risk-based strategies** rather than uniform cost management approaches

---

## 🛠 Tools & Technologies
- Tableau Desktop
- Microsoft PowerPoint (storytelling & presentation)
- GitHub (project documentation)

---

## 📁 Project Outputs
- Tableau Dashboard (`.twbx`)
- Presentation Slides (`.pptx`)
- Project Documentation (`README.md`)

---

## 📌 Conclusion
This project demonstrates how interactive dashboards and data-driven analysis can effectively identify high-cost patient segments and support better decision-making in healthcare cost management.
