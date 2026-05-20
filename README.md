# Student Performance Prediction using PySpark

A **Big Data Analytics** project that predicts student academic performance (Grade Class) using **Apache Spark (PySpark)** and a **Random Forest Classifier**, built and run on **Google Colab**.

The model achieved **88.57% accuracy** on a dataset of 2,392 students.

---

## Dataset

| Detail | Value |
|--------|-------|
| File | `validation.csv` |
| Rows | 2,392 students |
| Target Column | `GradeClass` (0–4) |

### Features Used

| Column | Description |
|--------|-------------|
| `Age` | Student age |
| `Gender` | 0 = Female, 1 = Male |
| `Ethnicity` | Encoded ethnicity (0–3) |
| `ParentalEducation` | Parent's education level (0–4) |
| `StudyTimeWeekly` | Weekly study hours |
| `Absences` | Number of absences |
| `Tutoring` | 1 = Yes, 0 = No |
| `ParentalSupport` | Level of parental support (0–4) |
| `Extracurricular` | 1 = Yes, 0 = No |
| `Sports` | 1 = Yes, 0 = No |
| `Music` | 1 = Yes, 0 = No |
| `Volunteering` | 1 = Yes, 0 = No |
| `GPA` | Grade Point Average |
| `GradeClass` | Target — 0 (A) to 4 (F) |

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Programming language |
| PySpark 3.5 | Distributed data processing |
| Spark MLlib | Machine learning pipeline |
| Pandas | Data conversion for visualization |
| Matplotlib & Seaborn | EDA visualizations |
| Google Colab | Cloud execution environment |

---

## Project Pipeline

```
Dataset (CSV)
    ↓
Data Loading (PySpark DataFrame)
    ↓
Data Cleaning (dropna, dropDuplicates, trim)
    ↓
RDD Operations (MapReduce — gender count, avg GPA)
    ↓
Exploratory Data Analysis (EDA)
    ↓
Feature Engineering (StringIndexer + VectorAssembler)
    ↓
Model Training (Random Forest — 80/20 split)
    ↓
Evaluation (88.57% Accuracy)
```

---

## What's Inside the Notebook

| Section | Details |
|---------|---------|
| Data Loading | Read CSV into Spark DataFrame, print schema |
| Data Cleaning | Remove nulls, duplicates, trim whitespace |
| RDD Operations | Gender count, average GPA using MapReduce |
| SQL-style Queries | GPA by ethnicity, top students by GPA, study time by parental education |
| EDA Visualizations | GPA distribution, Study Time vs GPA scatter, Gender bar chart, Avg GPA vs Parental Education |
| ML Pipeline | StringIndexer → VectorAssembler → RandomForestClassifier |
| Model Accuracy | **88.57%** on test set |

---

## How to Run

### Option 1 — Google Colab (Recommended)

1. Go to [Google Colab](https://colab.research.google.com)
2. Click **File → Upload Notebook** and upload `BDA_Mini_Project.ipynb`
3. Upload `validation.csv` when prompted by the file upload cell
4. Click **Runtime → Run All**

### Option 2 — Jupyter Notebook (Local)

**Prerequisites:**
```bash
pip install pyspark matplotlib seaborn pandas jupyter
```

**Run:**
```bash
jupyter notebook BDA_Mini_Project.ipynb
```

> **Note:** The notebook uses `google.colab.files.upload()` for file upload. If running locally, replace that cell with:
> ```python
> file_name = "validation.csv"
> ```

---

## Results

| Metric | Value |
|--------|-------|
| Model | Random Forest (50 trees) |
| Train / Test Split | 80% / 20% |
| **Accuracy** | **88.57%** |


---

## Author

**Thomson Sunny**  
GitHub: [@Thomson-4](https://github.com/Thomson-4)
