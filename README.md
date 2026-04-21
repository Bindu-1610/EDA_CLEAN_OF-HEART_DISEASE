# Heart Disease UCI Dataset — Data Cleaning & Visualization Project

This project performs **Data Cleaning**, **Exploratory Data Analysis (EDA)**, and **Data Visualization** on the **Heart Disease UCI Dataset** using Python in Jupyter Notebook.

#AIM:
    The aim is to understand medical data patterns and visualize relationships between health attributes and heart disease occurrence.
---

## 🎯 Project Objectives

* Import and explore dataset
* Clean inconsistent data
* Handle missing values
* Convert data types
* Perform exploratory data analysis
* Visualize important medical features

---

## 📂 Dataset Used

**File Name:** `heart_disease_uci.csv`

The dataset contains medical information of patients such as:

* Age
* Gender
* Blood pressure
* Cholesterol level
* Chest pain type
* Heart rate
* Heart disease status

---

## 🛠️ Tools & Technologies

* Python
* Jupyter Notebook
* Pandas
* Matplotlib
* Seaborn

---

## 📦 Required Libraries

Install dependencies before running the notebook:

```bash
pip install pandas matplotlib seaborn
```

---

## ▶️ Project Workflow
1️⃣ Import Libraries

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

---
2️⃣ Load Dataset

```python
df = pd.read_csv('heart_disease_uci.csv')
```

---
3️⃣ Display Dataset Information

```python
print(df.head())
print(df.info())
```

Purpose:

* View sample records
* Understand column types
* Check dataset structure

---
 4️⃣ Data Cleaning

Steps performed:

* Converted columns into numeric values
* Managed invalid entries
* Filled missing values using median

```python
df['age'] = pd.to_numeric(df['age'], errors='coerce')
df['chol'] = pd.to_numeric(df['chol'], errors='coerce')
df['trestbps'] = pd.to_numeric(df['trestbps'], errors='coerce')

df.fillna(df.median(numeric_only=True), inplace=True)
```
 📊 Data Visualization
✅ Heatmap

* Displays correlation between numerical health attributes.
* Helps identify important medical relationships.

---
✅ Bar Chart

**Heart Disease Distribution**

* Shows count of patients with and without heart disease.

---
✅ Box Plot

**Blood Pressure vs Heart Disease**

* Detects variation and possible outliers.

---

 ✅ Histogram

**Age Distribution**

* Displays frequency distribution of patient ages.

---

 ✅ Countplot  Analysis

**Gender vs Heart Disease**

* Compares disease occurrence among genders.

---
🔎 Key Insights

* Age plays an important role in heart disease risk.
* Blood pressure and cholesterol show noticeable patterns.
* Visualization helps identify relationships quickly.
* Clean data improves analysis accuracy.

---
📁 Project Structure

```
HeartDiseaseEDA/
│
├── heart_disease_uci.csv
├── EDA_CLEAN.ipynb
└── README.md
```

---
🚀 How to Run the Project

1. Download dataset from Kaggle
2. Place dataset file in project folder
3. Open Jupyter Notebook
4. Run all notebook cells sequentially

---
📚 Learning Outcomes

* Data Cleaning Techniques
* Exploratory Data Analysis
* Data Visualization using Seaborn
* Understanding Healthcare Data

---
✅ Final Output

The project successfully generates:

Cleaned medical dataset
Statistical understanding of features
Multiple visual insights
Patterns helpful for future machine learning prediction models


👩‍💻 Author
Modem.Himabindu
---
