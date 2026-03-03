📊 Scalable Multi-Class NOVA Classification Using Distributed Machine Learning
👩‍🎓 Module

7006SCN – Machine Learning and Big Data
MSc Data Science

📌 Project Overview

This project develops a scalable distributed machine learning pipeline to classify food products into NOVA processing groups (1–4) using the Open Food Facts dataset (>4GB).

The objective is to demonstrate:

Big Data ingestion using PySpark

Distributed MLlib model training

Custom feature engineering

Hyperparameter tuning with CrossValidator

Scalability analysis (strong & weak scaling)

Tableau dashboard visualisation

🗂 Dataset

Source: Open Food Facts (Hugging Face Repository)
https://huggingface.co/datasets/openfoodfacts/product-database

Size: 4.47 GB

Type: Semi-structured (Parquet format)

Target Variable: nova_group (multi-class classification)

The dataset contains structured nutritional attributes including:

Additives count

Ingredients count

Nutrient values (energy, sugars, fat, salt, proteins)

⚙️ Technologies Used

Python

PySpark (MLlib)

Scikit-learn (baseline comparison)

Google Colab

Tableau Public

🤖 Models Implemented

The following distributed MLlib models were trained and evaluated:

Logistic Regression

Decision Tree

Random Forest

One-vs-Rest Gradient Boosted Trees (Best Performing Model)

Evaluation metrics:

Accuracy

Weighted F1-score

Macro-F1

Confusion Matrix

Bootstrap Stability Analysis

📈 Key Results

Best Model: One-vs-Rest Gradient Boosted Trees

Accuracy: 0.8183

Weighted F1-score: 0.8129

Macro-F1: 0.7457

Boosting-based ensemble models outperformed linear and bagging-based methods for nonlinear nutritional data classification.

🚀 How to Run This Notebook
Option 1: Open in Google Colab

Upload the .ipynb file to Colab and run all cells.

Option 2: Local Environment

Requirements:

Python 3.9+

PySpark

scikit-learn

pandas

numpy

matplotlib

Install dependencies:

pip install pyspark scikit-learn pandas numpy matplotlib

Then run the notebook using Jupyter:

jupyter notebook
📊 Tableau Dashboards

Interactive dashboards are available via Tableau Public:

Data Quality & Preprocessing

Model Performance Evaluation

Business Insights

Scalability Analysis

(Insert your Tableau Public link here)

📉 Scalability Analysis

The project evaluates:

Shuffle partition tuning

Memory optimisation

Lineage checkpointing

Weak scaling (dataset growth)

Strong scaling (partition variation)

Results show shuffle operations are the primary computational bottleneck in distributed training.
