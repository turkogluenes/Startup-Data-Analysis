# Startup Success Analysis and Prediction 🚀

An end-to-end data science and machine learning project that analyzes factors influencing whether a startup gets **acquired** (success) or **closed**. This project performs comprehensive Exploratory Data Analysis (EDA) and builds a Random Forest Classifier to identify and predict the key drivers of startup outcomes.

---

## 📌 Project Overview

Understanding the factors that lead to startup success or failure is crucial for founders, investors, and policymakers. This project uses historical startup data to:
1. Clean and preprocess complex tabular startup metadata.
2. Conduct deep EDA to uncover patterns in geography, industry, funding, relationships, and age.
3. Quantify relationships via correlation analysis.
4. Train a **Random Forest Classifier** to predict startup acquisition.
5. Extract and visualize **Feature Importances** to pinpoint the most critical drivers of acquisition.

---

## 📊 Dataset Profile

The dataset (`startup data.csv`) contains profiles of **923 startups** with **49 initial features**, including:
* **Target Variable:** `status` (`acquired` vs. `closed`)
* **Temporal features:** Founding date, closing date, dates/ages at first and last funding/milestones.
* **Funding features:** Total funding (USD), number of funding rounds, presence of venture capital (VC) or angel funding, and round-specific markers (A, B, C, D).
* **Network & Quality indicators:** Number of relationships, milestones, top 500 status, and average participants.
* **Categorical markers:** State code, city, and industry categories (Software, Web, Mobile, Biotech, Enterprise, etc.).

---

## 🛠️ Tech Stack & Libraries

* **Language:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Visualization:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn` (Random Forest, train-test split, evaluations)
* **Environment:** Jupyter Notebook / VS Code

---

## 📂 Repository Structure

```directory
├── startup_analysis.ipynb   # Main Jupyter Notebook with step-by-step analysis and model
├── startup data.csv         # The raw dataset used for analysis
├── .gitignore               # Ignored local environments and temp files
└── README.md                # Project documentation (this file)
```

---

## 📈 Analysis Workflow & Key Steps

### 1. Data Cleaning
* Dropped redundant/identifier columns (`Unnamed: 0`, `Unnamed: 6`, `state_code.1`, `object_id`).
* Imputed missing values for milestone age features with standard defaults.

### 2. Exploratory Data Analysis (EDA)
* **Target Distribution:** Analyzed the balance between acquired and closed startups.
* **Geographic Trends:** Mapped state-level distributions (e.g., California (CA), New York (NY), Massachusetts (MA)) to see where successful startups cluster.
* **Industry Insights:** Explored performance across various tech categories (software, web, enterprise, biotech).
* **Funding & Relationship Dynamics:** Investigated how the volume of funding rounds, total USD raised, and the size of the startup's professional network (relationships) impact its success rate.

### 3. Machine Learning Modeling
* **Algorithm:** Random Forest Classifier.
* **Validation:** Train-test split on the dataset.
* **Performance Metrics:** Evaluated using a Classification Report (Precision, Recall, F1-Score), Confusion Matrix, and ROC-AUC score.
* **Feature Importance:** Extracted the feature importances to show exactly which variables (such as number of relationships, milestones, or early funding rounds) hold the highest predictive power.

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python installed, then set up your virtual environment and install the required dependencies:

```bash
# Clone the repository
git clone https://github.com/turkogluenes/Startup-Data-Analysis.git
cd Startup-Data-Analysis

# Create a virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Running the Notebook

Start Jupyter Notebook or open the project in VS Code to run the analysis:

```bash
jupyter notebook startup_analysis.ipynb
```

---

## 🔑 Key Findings & Takeaways

* **Relationships Matter:** The number of professional relationships and connections a startup builds is one of the strongest indicators of eventual acquisition.
* **Milestones as Validation:** Reaching key operational milestones early and often serves as a vital success signal for prospective acquirers.
* **Early Funding Strategy:** Startups that secure institutional backing (like Round A/B) or show high participant counts in funding rounds exhibit higher rates of success.
