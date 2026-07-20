# 🌱 Food Eco-Grade Prediction using Machine Learning and Deep Learning

## 📖 Overview

This repository contains the complete implementation of a research project investigating automatic prediction of food product **Eco-Grades (A+ to F)** using Natural Language Processing (NLP), Machine Learning, Deep Learning, and Transformer-based models.

The study uses textual information extracted from the **Open Food Facts** database to explore whether food eco-grades can be predicted without requiring expensive and time-consuming **Life Cycle Assessment (LCA)** calculations.

The repository includes the complete experimental pipeline, from data preprocessing and feature engineering to model training, evaluation, and comparison across multiple learning paradigms.

---

# 🎯 Research Objectives

The project investigates the following research questions:

- Can food eco-grades be accurately predicted using textual product information?
- How do classical Machine Learning models compare with Deep Learning and Transformer models?
- Does combining multiple product text fields improve predictive performance compared with ingredient information alone?
- Which modelling approach provides the best balance between predictive accuracy and minority-class performance?

---

# 📊 Dataset

**Source**

Open Food Facts Database

The processed dataset contains over **170,000 food products** with assigned Eco-Grade labels.

Target classes:

- A+
- A
- B
- C
- D
- E
- F

---

# 🧹 Data Preprocessing

Several preprocessing steps were performed before model training, including:

- Missing value handling
- Text cleaning and normalization
- Label encoding
- Train/test splitting
- Feature engineering

Different experiments investigate both:

- Ingredient-only representations
- Multi-field product representations combining:
  - Product name
  - Ingredient list
  - Ingredient hierarchy
  - Product category hierarchy

---

# 🧪 Experimental Design

This repository contains **five** experiments designed to progressively evaluate different feature representations and learning approaches.

## Experiment 1 — Ingredient-Based Baseline

- Data preprocessing
- Ingredient-only representation
- Classical Machine Learning baseline

Models evaluated:

- Naive Bayes
- SVM
- Logistic Regression
- Random Forest
- Extra Trees
- XGBoost

---

## Experiment 2 — Multi-field Product Representation

A richer textual representation was constructed by combining:

- Product name
- Ingredient list
- Ingredient hierarchy
- Product category hierarchy

Classical Machine Learning models were evaluated using this representation.

Models:

- Naive Bayes
- SVM
- Logistic Regression
- Random Forest
- Extra Trees
- XGBoost

---

## Experiment 3 — Feature Representation Comparison

Comparison of different text vectorisation techniques, including:

- Bag of Words (BoW)
- TF-IDF

An additional SMOTE experiment was conducted to investigate the impact of class balancing.

---

## Experiment 4 — Word2Vec + Bidirectional LSTM

Framework:

- TensorFlow
- Keras
- Gensim

Purpose:

Evaluate contextual word embeddings using a Bidirectional LSTM architecture.

---

## Experiment 5 — DistilBERT Transformer

Framework:

- Hugging Face Transformers
- PyTorch

Purpose:

Evaluate transformer-based language modelling for Eco-Grade prediction.

---

# 🤖 Models Evaluated

## Classical Machine Learning

- Naive Bayes
- Support Vector Machine (SVM)
- Logistic Regression
- Random Forest
- Extra Trees
- XGBoost

## Deep Learning

- Bidirectional LSTM
- Word2Vec Embeddings

## Transformer

- DistilBERT

---

# 📈 Evaluation Metrics

Model performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Macro F1-score
- Weighted F1-score
- Classification Report
- Confusion Matrix

---

# 🔍 Key Findings

The experiments demonstrate that:

- XGBoost achieved the strongest overall predictive performance among the evaluated classical Machine Learning models.
- Richer textual representations generally improved prediction performance compared with ingredient-only representations.
- The Bidirectional LSTM improved recognition of some minority classes but did not consistently outperform the best classical models.
- DistilBERT achieved competitive overall performance but showed weaker performance for the rare A+ class.
- Ensemble tree-based methods remain highly competitive for structured food-product text classification.

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow
- Keras
- PyTorch
- Hugging Face Transformers
- XGBoost
- Gensim (Word2Vec)
- Matplotlib
- Seaborn

---

# 📂 Repository Structure

```
Food-EcoGrade-Prediction/
│
├── Experiment_1_Ingredient_Baseline
├── Experiment_2_MultiField_Representation
├── Experiment_3_BoW_TFIDF_Comparison
├── Experiment_4_BiLSTM_Word2Vec
├── Experiment_5_DistilBERT
├── requirements.txt
└── README.md
```

---

# 🚀 Getting Started

Clone the repository:

```bash
git clone https://github.com/yourusername/Food-EcoGrade-Prediction.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run any experiment or open the provided Jupyter notebooks to reproduce the results.

---

# 📚 Citation

If you use this repository for research or academic purposes, please cite the associated publication or dissertation when available.

---

# 🙏 Acknowledgements

- Open Food Facts
- Birmingham City University
- TensorFlow
- PyTorch
- Hugging Face
- Scikit-learn
- XGBoost
