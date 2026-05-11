# Sentiment Analysis Project - README

## Overview

This project implements a sentiment analysis system for classifying movie reviews as either **positive** or **negative** using supervised machine learning. It is based on the Cornell Movie Review Polarity Dataset (v2.0) and developed as part of a computational linguistics course project.

## Contents

* `sentiment_analysis_project.ipynb` — Main notebook with preprocessing, feature engineering, modeling, evaluation, and error analysis.
* `model_performance_summary.csv` — Summary table comparing performance of different vectorization strategies.
* `report.pdf` — Final report outlining methodology, results, and analysis.
* `Data/` — Folder containing `review_polarity.tar.gz` dataset and extracted reviews.

## Installation

1. Clone the repo or download the files.
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Ensure you have the `en_core_web_sm` SpaCy model:

   ```bash
   python -m spacy download en_core_web_sm
   ```

## How to Run

1. Start Jupyter Notebook or run the Python script.
2. Load and preprocess the dataset using:

   ```python
   data, labels = load_data("../Data/review_polarity.tar.gz")
   ```
3. Train models:

   * Run `baseline_model(...)`
   * Evaluate using `compare_models(...)`
   * Explore feature variants with `feature_engineering(...)`
   * Analyze errors via `error_analysis(...)`
   * Optional: Evaluate syntax-aware model with `evaluate_syntax_model(...)`

## Features Implemented

* CountVectorizer and TfidfVectorizer with different configurations
* Naive Bayes, Logistic Regression, Decision Tree, Random Forest classifiers
* Syntax-aware negation feature extraction using SpaCy
* Evaluation metrics: accuracy, precision, recall, F1-score, confusion matrix
* Training time and feature count comparison

## Acknowledgments

* Dataset: movie review dataset from Cornell
* SpaCy, scikit-learn, NLTK libraries
* Instructor and TAs for providing starter code