# Scalable Multi-Class NOVA Classification Using Distributed Machine Learning

## Project Overview

This project develops a **scalable distributed machine learning pipeline** to classify food products into **NOVA processing groups (1–4)** using the Open Food Facts dataset (>4GB).
The main code file is **ML_and_BigData_Project_OpenFoodFacts_NOVA.ipynb**

### Objectives

The project demonstrates:

- Big Data ingestion using **PySpark**
- Distributed **MLlib** model training
- Custom feature engineering
- Hyperparameter tuning with **CrossValidator**
- Scalability analysis (strong & weak scaling)
- Interactive **Tableau dashboard visualisation**

---

## Dataset

**Source:**  
https://huggingface.co/datasets/openfoodfacts/product-database  

- **Dataset:** Open Food Facts (Hugging Face Repository)
- **Size:** 4.47 GB
- **Format:** Semi-structured (Parquet)
- **Target Variable:** `nova_group` (Multi-class classification)

### Features Used

The dataset includes structured nutritional attributes such as:

- Additives count
- Ingredients count
- Nutrient values (energy, sugars, fat, salt, proteins)

---

## Technologies Used

- Python
- PySpark (MLlib)
- Scikit-learn (baseline comparison)
- Google Colab
- Tableau Public

---

## Models Implemented

The following distributed MLlib models were trained and evaluated:

1. Logistic Regression  
2. Decision Tree  
3. Random Forest  
4. One-vs-Rest Gradient Boosted Trees (**Best Performing Model**)

### Evaluation Metrics

- Accuracy
- Weighted F1-score
- Macro-F1
- Confusion Matrix
- Bootstrap Stability Analysis

---

## Key Results

- **Best Model:** One-vs-Rest Gradient Boosted Trees  
- **Accuracy:** 0.8183  
- **Weighted F1-score:** 0.8129  
- **Macro-F1:** 0.7457  

Boosting-based ensemble models outperformed linear and bagging-based approaches in modelling nonlinear nutritional interactions.

**Tableau Public Link:**  
*(Insert your Tableau workbook link here)*  

---

---

## How to Run the Project

### Option 1: Run in Google Colab

1. Upload the `.ipynb` file to Google Colab  
2. Run all cells  

---

### Option 2: Run Locally

#### Requirements

- Python 3.9+
- PySpark
- scikit-learn
- pandas
- numpy
- matplotlib

#### Install Dependencies

```bash
pip install pyspark scikit-learn pandas numpy matplotlib
