# 🎬 NLP & Sentiment Analysis — IMDB Movie Reviews

![Python](https://img.shields.io/badge/Python-3.12-blue?style=flat-square&logo=python)
![NLTK](https://img.shields.io/badge/NLTK-NLP-green?style=flat-square)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=flat-square)
![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20BEFF?style=flat-square&logo=kaggle)
![Accuracy](https://img.shields.io/badge/Accuracy-86.93%25-brightgreen?style=flat-square)

> A production-grade NLP pipeline that mathematically decodes human sentiment from 50,000 IMDB movie reviews using Multinomial Naive Bayes classification.

---

## 📌 Project Overview

80% of enterprise data exists in unstructured text format — invisible to traditional analytics. This project bridges that gap by building a strict text pre-processing and classification pipeline that transforms raw human language into quantitative spatial representations to predict emotional polarity.

**DecodeLabs Data Science Internship | Project 4 | Week 5**

---

## 🏗️ Pipeline Architecture
| Step | Technique | Output |
|------|-----------|--------|
| 1. Ingest | Load 50K IMDB reviews | Raw strings |
| 2. Pre-Process | Tokenization + Custom Stop-words + POS Lemmatization | Clean tokens |
| 3. Vectorize | TF-IDF (Unigrams + Bigrams), max_features=10000 | CSR Sparse Matrix |
| 4. Model | Multinomial Naive Bayes (alpha=1.0) | Probability Distribution |

---

## ⚙️ Key Engineering Decisions

- **Negations preserved** — Excluded `not`, `never`, `don't` etc. from stopword lists using set-based operations to prevent sentiment reversal (e.g. "not good" stays negative)
- **POS-guided Lemmatization** — Part-of-Speech tags passed to WordNetLemmatizer for morphologically accurate root extraction ("went" → "go")
- **SciPy CSR Sparse Format** — 99.04% zero matrix stored efficiently, saving gigabytes of RAM
- **Laplace Smoothing (alpha=1.0)** — Zero-frequency problem solved; no probability ever becomes absolute zero

---

## 📊 Results

| Metric | Negative | Positive |
|--------|----------|----------|
| Precision | 0.88 | 0.86 |
| Recall | 0.86 | 0.88 |
| F1-Score | 0.87 | 0.87 |
| **Accuracy** | **86.93%** | |

---

## 🧪 Live Prediction Test

| Review | Prediction | Confidence |
|--------|------------|------------|
| "This movie was absolutely amazing!" | POSITIVE | 62.6% |
| "Terrible movie. Complete waste of time." | NEGATIVE | 99.2% |
| "I did not enjoy this film at all." | POSITIVE | 62.1% |

---

## 🛠️ Tech Stack

| Library | Purpose |
|---------|---------|
| NLTK | Tokenization, POS tagging, Lemmatization |
| Scikit-learn | TF-IDF Vectorization, Naive Bayes, Metrics |
| SciPy | CSR Sparse Matrix storage |
| Pandas | Data manipulation |
| Matplotlib / Seaborn | Visualization |

---

## 📁 Dataset

[IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) — Perfectly balanced: 25,000 positive + 25,000 negative reviews.

---

## 🔗 Links

- 📓 [Kaggle Notebook](https://www.kaggle.com/code/muqaddasimtiaz)
- 👤 [GitHub](https://github.com/Muqadas-g)
- 💼 [LinkedIn](https://www.linkedin.com/in/muqaddas-imtiaz)

---

*"I don't just study Data Science — I build real-world intelligent systems!"*
