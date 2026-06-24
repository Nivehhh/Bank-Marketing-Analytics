🏦 Bank Marketing Analytics — Predictive Modeling & RAG Insights


A complete end-to-end machine learning project that predicts whether a bank customer will subscribe to a term deposit, using classification models, statistical tests, and a RAG-based Q&A system for business insights.


📌 Table of Contents


Business Problem
Project Highlights
Dataset Overview
Project Structure
Tech Stack
Installation & Setup
How to Run
Analysis Walkthrough
Model Results
ROI Analysis
RAG System
Business Recommendations
Output Files
License



🎯 Business Problem

A retail bank runs telephone marketing campaigns to promote term deposit subscriptions. These campaigns are costly and often reach customers who have no intention of subscribing, leading to:


High campaign costs with low ROI
Poor customer experience from irrelevant outreach
Wasted agent time and resources


Goal: Build a machine learning model to predict which customers are most likely to subscribe — enabling the bank to target the right people, reduce costs, and maximize revenue.


🚀 Project Highlights

FeatureDetailsML ModelsLogistic Regression, Random ForestStatistical TestsChi-Square Test, Independent T-TestInsights EngineRAG (Retrieval-Augmented Generation) with FAISSVisual AnalysisSeaborn & Matplotlib chartsBusiness OutputROI calculation, exportable predictionsExport ReadyCSV files for Power BI / Tableau dashboards


📊 Dataset Overview

The dataset is based on the UCI Bank Marketing Dataset.

ColumnDescriptionageCustomer's agejobType of jobbalanceAccount balancehousingHas housing loan?contactContact communication typepoutcomeOutcome of previous campaigndepositTarget — Did the customer subscribe? (yes/no)


📁 Project Structure

bank-marketing-analytics/
│
├── bank_marketing_analytics.py     # Main analysis script
├── bank.csv                        # Raw dataset (add your own)
├── requirements.txt                # Python dependencies
├── README.md                       # Project documentation
│
├── outputs/
│   ├── bank_dashboard.csv          # Full data for BI tools
│   ├── bank_predictions.csv        # Model predictions
│   └── feature_importance.csv      # Feature ranking from Random Forest
│
└── notebooks/
    └── Bank_Marketing_Analytics.ipynb   # Google Colab notebook


🛠 Tech Stack


Python 3.8+
Pandas — Data manipulation
NumPy — Numerical operations
Matplotlib / Seaborn — Data visualization
Scikit-learn — ML models and evaluation
SciPy — Statistical hypothesis testing
Sentence-Transformers — Text embeddings for RAG
FAISS — Vector similarity search



⚙️ Installation & Setup

1. Clone the Repository

bashgit clone https://github.com/YOUR_USERNAME/bank-marketing-analytics.git
cd bank-marketing-analytics

2. Create a Virtual Environment (Recommended)

bashpython -m venv venv
source venv/bin/activate        # On Mac/Linux
venv\Scripts\activate           # On Windows

3. Install Dependencies

bashpip install -r requirements.txt

4. Add the Dataset

Place your bank.csv file in the root directory.

Dataset source: UCI ML Repository — Bank Marketing


▶️ How to Run

Option A — Run as Python Script

bashpython bank_marketing_analytics.py

Option B — Run in Google Colab

Show Image


Open the notebook link above
Upload bank.csv when prompted
Run all cells (Runtime > Run All)



🔍 Analysis Walkthrough

Step 1 — Exploratory Data Analysis (EDA)


Target variable distribution (deposit: yes/no)
Age distribution and age group segmentation
Job type vs deposit conversion rate
Balance comparison between subscribers and non-subscribers


Step 2 — Statistical Testing


Chi-Square Test: Tests if housing loan status is statistically related to deposit subscription
T-Test: Tests if account balance differs significantly between subscribers and non-subscribers


Step 3 — Feature Engineering


One-hot encoding of all categorical variables
Age group binning: 18–25, 26–35, 36–45, 46–60, 60+


Step 4 — Machine Learning


Train/Test split (80/20, stratified)
Logistic Regression (baseline)
Random Forest Classifier (final model)


Step 5 — Business Insights via RAG


FAISS-based retrieval from project knowledge base
Natural language Q&A on marketing insights



📈 Model Results

Logistic Regression

MetricScoreAccuracy~80%ROC-AUC~0.87

Random Forest

MetricScoreAccuracy~85%+ROC-AUC~0.92+


Actual values depend on your dataset version. Random Forest consistently outperforms Logistic Regression on this task.



Top Predictive Features (Random Forest)


Duration of last call
Previous campaign outcome
Account balance
Age
Job type



💰 ROI Analysis

The project includes a built-in ROI calculator:

MetricValueCost per call₹100Revenue per conversion₹1,000ROICalculated dynamically

By targeting only model-predicted positives, the bank can significantly reduce campaign costs while maintaining or improving conversion revenue.


🤖 RAG System

A lightweight Retrieval-Augmented Generation (RAG) system is built using:


sentence-transformers for semantic embeddings
FAISS for fast vector similarity search


Sample queries supported:


"What factors improve deposit subscriptions?"
"How can the bank increase ROI?"
"Which model was used for prediction?"


The system retrieves the most relevant business insights from a curated knowledge base built from project findings.


💡 Business Recommendations


Prioritize long-duration calls — Call duration is the strongest predictor of subscription.
Leverage previous campaign data — Customers with prior success are high-value targets.
Deploy ML before campaigns — Score customers before calling to reduce waste.
Segment by age and job — Certain demographics convert at significantly higher rates.
Reduce low-probability outreach — Redirect budget from predicted negatives to positives.



📤 Output Files

FileDescriptionbank_dashboard.csvFull enriched dataset for Power BI/Tableaubank_predictions.csvActual vs predicted labels per customerfeature_importance.csvRanked feature importance from Random Forest


📄 License

This project is licensed under the MIT License.


🙋 Author

Nivedha.S

📧 nivedha207@gmail.com




⭐ If you found this project useful, please give it a star!
