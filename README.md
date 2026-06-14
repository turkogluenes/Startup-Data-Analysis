# Startup Success Analysis and Prediction

This project analyzes the factors that influence whether a startup succeeds (gets acquired) or closes down. I performed exploratory data analysis (EDA) and trained a Random Forest model on a startup dataset to identify the key drivers of these outcomes.

## Project Description

Understanding why startups succeed or fail is a common topic in entrepreneurship and data science. In this project, I used a historical startup dataset to:
1. Clean and preprocess the tabular data.
2. Conduct exploratory data analysis to look at relationships between startup features (like location, funding rounds, relationships) and their final status.
3. Train a Random Forest Classifier to predict if a startup will be acquired.
4. Extract feature importances to see which factors contribute the most to startup success.

## Dataset Info

The dataset used is `startup data.csv`, which has 923 rows and 49 columns. Some of the main features include:
* **Target Variable:** `status` (either `acquired` or `closed`).
* **Funding Features:** Total funding in USD, number of funding rounds, angel investment, venture capital (VC) backing, and rounds (A, B, C, D).
* **Company Profile:** Found date, age at first and last funding, location (state and city), and industry category (software, web, mobile, biotech, etc.).
* **Network Features:** Number of relationships, milestones reached, and average participant count in funding.

## Dependencies

The project uses Python 3 along with the following libraries:
* `pandas` and `numpy` for data cleaning and manipulation.
* `matplotlib` and `seaborn` for plotting and visualization.
* `scikit-learn` for splitting the data, training the Random Forest model, and evaluating performance.

## Project Structure

* `startup_analysis.ipynb`: The main Jupyter Notebook containing the code for EDA, data cleaning, and modeling.
* `startup data.csv`: The dataset containing startup records.
* `.gitignore`: Configured to ignore the virtual environment (`.venv`) and checkpoint files.
* `README.md`: This file.

## Steps Completed

### 1. Data Cleaning
* Dropped unnecessary columns like `Unnamed: 0`, `Unnamed: 6`, `state_code.1`, and `object_id`.
* Replaced missing values in milestone age columns with 0.

### 2. Exploratory Data Analysis (EDA)
* Plotted the class distribution of the target variable (`status`).
* Checked how startups are distributed across different states (e.g., CA, NY, MA) and tech industries.
* Analyzed relationships between funding amounts, funding rounds, and startup success.

### 3. Machine Learning and Evaluation
* Split the dataset into training and testing sets.
* Trained a Random Forest Classifier.
* Evaluated the model using precision, recall, F1-score, confusion matrix, and ROC-AUC score.
* Plotted the feature importances to identify the most significant features.

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/turkogluenes/Startup-Data-Analysis.git
   cd Startup-Data-Analysis
   ```

2. Set up a virtual environment and install dependencies:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook startup_analysis.ipynb
   ```

## Key Findings

* **Relationships:** The number of professional relationships or network connections is one of the strongest indicators of startup success.
* **Milestones:** Startups that reach their first and last milestones have higher acquisition rates.
* **Funding Rounds:** Having active early-stage funding rounds (like Round A and B) correlates positively with a startup being acquired.
