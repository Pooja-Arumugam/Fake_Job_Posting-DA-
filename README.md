# 🕵️‍♀️ Fake Job Postings Fraud Detection

This project analyzes thousands of online job postings to detect fraudulent listings. Using **Python**, **R**, and **Excel**, it combines data cleaning, anomaly detection, exploratory analysis, machine learning, and an interactive dashboard.

---

## 🎯 Project Motivation

The internet has transformed the job search process, but it has also enabled scammers to publish fake job ads to steal identities, collect personal data, and defraud applicants. Detecting these fraudulent postings is critical to protect job seekers and maintain trust in online job boards.

---

## 🗂️ Dataset

**Source:** [Kaggle – Fake Job Postings Dataset](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction)  
- **Records:** ~18,000 job postings  
- **Columns:** 18 fields (job title, company profile, description, employment type, required experience, fraud label, etc.)  
- **Fraudulent Label:**  
  - `0 = Real`
  - `1 = Fake`

---

## 🛠️ Technologies Used

The project leveraged different tools for their strengths:

### 🐍 Python
Used for:
- **Data Preprocessing**
  - Cleaning missing values
  - Removing duplicates
  - Imputing unknowns
  - Handling outliers
- **Exploratory Data Analysis**
  - Distribution plots and violin plots
  - Correlation heatmaps
  - WordCloud visualizations of frequent terms
- **Anomaly Detection**
  - Flagging rare job functions
  - Identifying unusually short or long descriptions
- **Machine Learning**
  - Training a Random Forest classifier
  - Handling class imbalance with `class_weight="balanced"`
  - Model evaluation with precision, recall, F1-score, and confusion matrix

**Key Libraries:**  
`pandas`, `numpy`, `matplotlib`, `seaborn`, `WordCloud`, `scikit-learn`

---

### 📊 R
Used for:
- **Summary Statistics**
  - Pivot tables to compare fraud rates by employment type and experience level
- **Interactive Dashboard**
  - Built in **R Shiny** for dynamic filtering and visualization of fraud patterns
- **Descriptive Analytics**
  - Grouping and summarizing categorical features

**Key Packages:**  
`tidyverse`, `dplyr`, `shiny`, `ggplot2`

---

### 🟢 Excel
Used for:
- Initial data inspection
- Validating row and column completeness
- Cross-checking summary counts and pivot tables to ensure consistency across tools

---

## 📂 Project Structure

```
├── FinalProject.Rproj
├── Project(sda).ipynb
├── README.md
├── arumugam_finalproject(report).pdf
├── arumugam_final-project-r-program-pivot-and-dashboard.pdf
├── fake_job_postings.zip
├── final-project-r-program-pivot-and-dashboard.pdf
├── job_fraud.zip
├── rpogpart(knit pdf file).pdf
```


---

## 🔍 Workflow Overview

1️⃣ **Data Cleaning (Python)**
- Imputed missing fields as "Unknown"
- Removed duplicate entries
- Detected and removed outliers using IQR filtering

2️⃣ **EDA (Python)**
- Violin plots showing description length distributions
- Correlation heatmaps identifying relationships with fraud
- WordClouds visualizing frequent terms in real vs fake descriptions

3️⃣ **Anomaly Detection (Python)**
- Flagged rare job functions (appearing <40 times)
- Identified suspicious patterns (missing experience and employment type)

4️⃣ **Modeling (Python)**
- Random Forest classifier achieved:
  - **Accuracy:** ~96%
  - **F1-Score (Fraud):** 0.67
  - Balanced weighting to improve fraud detection sensitivity

5️⃣ **Pivot Tables and Summaries (R)**
- Cross-tabulations of fraud vs employment type and experience

6️⃣ **Interactive Dashboard (R Shiny)**
- Dynamic filtering by job type and industry
- Visual exploration of fraud patterns

7️⃣ **Validation (Excel)**
- Checked summary counts and pivot table results

---

## 🏆 Project Outcomes (STAR Format)

- **Analyzed** an imbalanced dataset of ~18,000 postings to detect fraud by building a Random Forest model in Python, achieving **96% accuracy**.
- **Faced** vague, incomplete descriptions requiring pattern discovery, performed EDA with WordClouds and violin plots to uncover fraud indicators.
- **Identified** the need for clear fraud visualization for stakeholders, developed an R Shiny dashboard enabling interactive exploration.
- **Encountered** significant missing values and outliers needing cleanup, applied imputation and IQR filtering to create a reliable dataset.

---

## 📈 Key Insights

- Fake postings are often labeled **Full-time** to appear credible.
- Fraud is more frequent in **IT, Internet, and Services** industries.
- Vague experience requirements and generic wording are strong fraud indicators.
- Unusually short or long descriptions correlate with scams.

---

## 🚀 How to Run the Project

####Set Up Python Environment
Install dependencies
Open and run the notebook:
- jupyter notebook "Project(sda).ipynb"

#### Run R Analysis
Open FinalProject.Rproj in RStudio:
- Run R scripts for pivot tables
- Launch the dashboard:
          shiny::runApp()
#### Use Excel (Optional)
Open the dataset in Excel to validate data summaries and pivot tables.

## 💡 Future Improvements
- Use NLP embeddings (TF-IDF, BERT) for better text classification
- Implement oversampling (SMOTE) to improve minority class recall
- Integrate real-time fraud scoring into the dashboard


### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/fake-job-fraud-detection.git
cd fake-job-fraud-detection
