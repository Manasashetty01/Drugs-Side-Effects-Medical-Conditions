# 💊 Drugs, Side Effects & Medical Conditions — Analysis

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![EDA](https://img.shields.io/badge/Exploratory-Data%20Analysis-green)
![License](https://img.shields.io/badge/License-MIT-success)

---

## 📌 Project Overview

This project explores **drug reviews, side effects, and medical conditions** using user-contributed data from *Drugs.com*.

The workflow involved:

* Cleaning and preparing the dataset.
* Creating new features such as **review score, side effect count, and effectiveness categories**.
* Performing **Exploratory Data Analysis (EDA)** to study drug ratings, review volumes, side effects, and correlations.
* Summarizing **key insights, limitations, and recommendations** for future work.

📊 *Dataset size:* **2,931 records × 20 columns**

---

## 🗂 Dataset Description

Key columns in the dataset:

| Feature              | Description                 |
| -------------------- | --------------------------- |
| `drug_name`          | Name of the drug            |
| `medical_condition`  | Condition treated           |
| `side_effects`       | Reported side effects       |
| `generic_name`       | Generic version of the drug |
| `drug_classes`       | Drug classification         |
| `brand_names`        | Brand names                 |
| `rating`             | User rating                 |
| `no_of_reviews`      | Number of reviews           |
| `pregnancy_category` | Safety in pregnancy         |
| `alcohol`            | Alcohol interaction info    |

---

## 🧹 Data Cleaning

* Filled missing **brand\_names, related\_drugs, alcohol, rating, and reviews** with placeholders (`"Unknown"`, `"None"`, `"Not Specified"`, or `0`).
* Standardized text columns (lowercase, removed whitespace).
* Converted categorical variables into categories.
* Retained all records for complete coverage.

---

## ⚙️ Feature Engineering

* **Review Score** → `rating × no_of_reviews` (measures popularity × quality).
* **Side Effect Count** → number of reported side effects per drug (median = 27, max = 1,394).
* **Effectiveness** (based on rating):

  * High (≥ 8)
  * Medium (≥ 5)
  * Low (> 0 & < 5)
  * Unrated (0)

---

## 📊 Exploratory Data Analysis — Key Findings

* **Rating distribution:** Mean = 6.93, Median = 7.05; most drugs fall between 6–9.
* **Top reviewed drugs:**

  * Phentermine — 2,934 reviews, rating 8.7
  * Contrave — 1,939 reviews, rating 6.6
  * Escitalopram — 1,471 reviews, rating 7.4
* **Effectiveness categories:** Unrated (1,371), Medium (746), High (570), Low (244).
* **Common side effects:** Hives, nausea, vomiting, itching, dizziness, diarrhea.
* **Correlation:** Weak positive correlation (r ≈ 0.218) between reviews and ratings → popularity ≠ higher quality.
* **Heatmap insights:** Common side effects overlap across multiple top drugs (e.g., hives, nausea, dizziness).

---

## 💡 Insights

✔️ Most ratings are moderate (6–9).

✔️ Weight-loss & antidepressant drugs dominate review counts.

✔️ Many `"Unknown"` entries highlight missing data.

✔️ Text parsing created noise (e.g., “lips”, “tongue” as side effects).

✔️ High review counts do not guarantee higher ratings.

---

## 🚧 Limitations

* Free-text side effect parsing introduced artifacts.
* Setting missing ratings to `0` inflated “Unrated” drugs.
* Reviews are **user-reported** → subjective and unverified.

---

## 🚀 Future Work

* Use **NLP** for cleaning side effect text.
* Group drugs by **class** or **indication** for comparisons.
* Perform **sentiment analysis** on review text.
* Apply advanced ML models (Random Forest, Gradient Boosting) to predict ratings/effectiveness.

---

## 📂 Repository Structure

```bash
📦 Drugs-SideEffects-Analysis
 ┣ 📜 README.md
 ┣ 📂 data
 ┃ ┗ drugs_side_effects.csv
 ┣ 📂 notebooks
 ┃ ┗ drugs_analysis.ipynb
 ┣ 📂 reports
 ┃ ┗ Drugs, Side Effects & Medical Conditions.docx
```

---

## 🛠 Tools & Technologies

* **Python** (Pandas, Numpy, Matplotlib, Seaborn)
* **Jupyter Notebook**
* **Exploratory Data Analysis (EDA)**

---

## 📜 License

MIT License.

---

✨ If you found this project useful, please ⭐ star the repo!


