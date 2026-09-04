# YuvaIntern Week 3 – Feature Engineering

## 📌 Project Overview

This project was completed as part of the **YuvaIntern Data Science Internship – Week 3 Task: Feature Engineering**.

The objective was to create meaningful new features from an existing **food processing and nutrition dataset** and evaluate their usefulness for future data analysis and machine-learning workflows.

The project includes the completed Jupyter Notebook, final feature-engineered dataset, internship report, and screenshots of the notebook outputs.

---

## 👤 Internship Details

| Detail | Information |
|---|---|
| **Student** | Vibhuti Prajapati |
| **Program** | Master of Computer Applications (MCA) |
| **Institution** | UIT-RGPV |
| **Role** | Data Science Intern |
| **Organization** | YuvaIntern |
| **Task** | Week 3 – Feature Engineering |
| **Submission Date** | 3 September 2026 |

---

## 🎯 Objectives

- Understand the structure of the food nutrition dataset.
- Prepare the data before creating derived features.
- Brainstorm meaningful feature combinations and ratios.
- Create new numerical features from existing nutrition variables.
- Evaluate the engineered features using descriptive statistics.
- Validate the new features for missing and infinite values.
- Export the final feature-engineered dataset.

---

## 📊 Dataset

The project uses a food nutrition dataset containing product information, processing-related attributes, and nutritional values per 100 g.

### Original Dataset

- **Rows:** 9,804
- **Columns:** 20

### Final Feature-Engineered Dataset

- **Rows:** 9,771
- **Columns:** 25
- **Missing values:** 0
- **Duplicate rows:** 0
- **Engineered features:** 8

---

## 🧹 Data Preparation

Before feature engineering, the notebook performed:

1. Dataset inspection
2. Numerical missing-value treatment using median imputation
3. Categorical missing-value treatment using mode imputation
4. Removal of unnecessary columns:
   - `code`
   - `product_name`
   - `ingredients_text`
5. Duplicate removal
6. IQR-based outlier capping
7. Final data validation

---

## ⚙️ Feature Engineering

Eight new features were created:

### 1. `total_macronutrients`

Combines:

```text
fat + carbohydrates + proteins
```

This provides an aggregate measure of recorded macronutrient content.

### 2. `sugar_carb_ratio`

```text
sugars / carbohydrates
```

Used to represent the relative proportion of carbohydrates accounted for by sugars.

### 3. `saturated_fat_ratio`

```text
saturated fat / total fat
```

Used to represent the relative share of saturated fat within total fat.

### 4. `fiber_carb_ratio`

```text
fiber / carbohydrates
```

Used to represent fiber relative to recorded carbohydrates.

### 5. `protein_energy_pct`

```text
(protein × 4 / energy) × 100
```

An energy-relative representation of protein using the notebook's calculation.

### 6. `carb_energy_pct`

```text
(carbohydrates × 4 / energy) × 100
```

An energy-relative representation of carbohydrates.

### 7. `fat_energy_pct`

```text
(fat × 9 / energy) × 100
```

An energy-relative representation of fat.

### 8. `macronutrient_balance`

```text
(protein + carbohydrates) / (fat + 1)
```

Creates a numerical relationship between protein/carbohydrate content and fat content.

> **Note:** These are analytical features created for the dataset and are not intended as clinical or individualized nutrition recommendations.

---

## 📈 Feature Evaluation

The engineered features were evaluated using:

- Mean
- Median
- Minimum
- Maximum
- Missing-value check
- Infinite-value check

### Key Results

| Feature | Mean | Median | Minimum | Maximum |
|---|---:|---:|---:|---:|
| `total_macronutrients` | 50.064 | 48.880 | 0.000 | 116.428 |
| `sugar_carb_ratio` | 0.429 | 0.359 | 0.000 | 1.000 |
| `saturated_fat_ratio` | 0.286 | 0.214 | 0.000 | 1.000 |
| `fiber_carb_ratio` | 0.228 | 0.112 | 0.000 | 1.000 |
| `protein_energy_pct` | 12.904 | 8.857 | 0.000 | 100.000 |
| `carb_energy_pct` | 44.756 | 46.275 | 0.000 | 100.000 |
| `fat_energy_pct` | 34.052 | 30.638 | 0.000 | 100.000 |
| `macronutrient_balance` | 8.181 | 3.085 | 0.000 | 101.430 |

---

## ✅ Validation

Final validation confirmed:

```text
Rows: 9771
Columns: 25
Missing values: 0
Duplicate rows: 0
Infinite values in engineered features: 0
```

The final feature-engineered dataset was successfully exported as:

```text
food_processing_feature_engineered.csv
```

---
## Notebook Screenshots

### 1. Dataset Overview

<img src="https://raw.githubusercontent.com/vibhutip513-commits/YuvaIntern_week3-foood-data-feacher-engineering/main/screenshots/01_dataset_overview.png" alt="Dataset Overview" width="900">

### 2. Data Preprocessing

<img src="https://raw.githubusercontent.com/vibhutip513-commits/YuvaIntern_week3-foood-data-feacher-engineering/main/screenshots/02_data_preprocessing.png" alt="Data Preprocessing" width="900">

### 3. Data Preparation

<img src="https://raw.githubusercontent.com/vibhutip513-commits/YuvaIntern_week3-foood-data-feacher-engineering/main/screenshots/03_data_preparation.png" alt="Data Preparation" width="900">

### 4. Feature Engineering – Part 1

<img src="https://raw.githubusercontent.com/vibhutip513-commits/YuvaIntern_week3-foood-data-feacher-engineering/main/screenshots/04_feature_engineering_part1.png" alt="Feature Engineering Part 1" width="900">

### 5. Feature Engineering – Part 2

<img src="https://raw.githubusercontent.com/vibhutip513-commits/YuvaIntern_week3-foood-data-feacher-engineering/main/screenshots/05_feature_engineering_part2.png" alt="Feature Engineering Part 2" width="900">

### 6. Feature Evaluation

<img src="https://raw.githubusercontent.com/vibhutip513-commits/YuvaIntern_week3-foood-data-feacher-engineering/main/screenshots/06_feature_evaluation.png" alt="Feature Evaluation" width="900">

### 7. Validation

<img src="https://raw.githubusercontent.com/vibhutip513-commits/YuvaIntern_week3-foood-data-feacher-engineering/main/screenshots/07_validation.png" alt="Validation" width="900">

### 8. Final Results

<img src="https://raw.githubusercontent.com/vibhutip513-commits/YuvaIntern_week3-foood-data-feacher-engineering/main/screenshots/08_final_results.png" alt="Final Results" width="900">

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📁 Project Structure

```text
YuvaIntern_week3-feature-engineering/
│
├── week3.ipynb
├── food_processing_feature_engineered.csv
├── Week_3_Food_Processing_Feature_Engineering_Report_YuvaIntern_Professional.docx
├── README.md
│
└── screenshots/
    ├── Dataset_Overview.png
    ├── Data_Preparation.png
    ├── Data_Preprocessing.png
    ├── Feature_Engineering_Part_1.png
    ├── Feature_Engineering_Part_2.png
    ├── Feature_Evaluation.png
    ├── Validation.png
    └── Results_-_Final_Dataset.png
```

---

## 📄 Project Files

### Jupyter Notebook
`week3.ipynb`

Contains the complete data preparation, feature engineering, evaluation, validation, and export workflow.

### Final Dataset
`food_processing_feature_engineered.csv`

Contains the final feature-engineered dataset with 9,771 rows and 25 columns.

### Internship Report
`Week_3_Food_Processing_Feature_Engineering_Report_YuvaIntern_Professional.docx`

Contains the detailed Week 3 report with methodology, feature explanations, evaluation, and notebook screenshots.

---

## 🏁 Conclusion

The Week 3 Feature Engineering task was completed successfully. Eight derived features were created from the food nutrition dataset using aggregate, ratio, and energy-based transformations.

The final dataset contains **9,771 records and 25 columns**, with **zero missing values**, **zero duplicate rows**, and **no infinite values in the engineered features**.

The resulting dataset is prepared for further exploratory analysis, feature selection, and machine-learning experiments.

---

## 👨‍💻 Author

**Vibhuti Prajapati**  
MCA – UIT-RGPV  
Data Science Intern – YuvaIntern
# YuvaIntern_week3-fooood-data-feacher-enginering
