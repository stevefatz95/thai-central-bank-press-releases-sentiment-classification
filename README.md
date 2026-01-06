# Sentiment Classification of Thai Central Bank Press Releases Using Supervised Learning

This repository contains the dataset and reference notebook used in:

**Grassi, S. (2025). _Sentiment Classification of Thai Central Bank Press Releases Using Supervised Learning_.**  
arXiv:2503.22629 — [arXiv Link](https://arxiv.org/abs/2503.22629)


The materials are intended for **research, education and applied NLP practice** in the context of central bank communication.

---

## Contents

- **`bot_annotated_sentences.csv`**  
  Annotated corpus of sentences extracted from English-language press releases issued by the Bank of Thailand.

- **`thai_cb_sentiment_classification.ipynb`**  
  Jupyter Notebook used to generate the analysis and results reported in the paper.

---

## Dataset Summary

- **794 pre-labeled sentences**
- Extracted from **26 Monetary Policy Committee press releases**
- Coverage: **Feb 2021 – Dec 2024**
- Sentence-level sentiment labels
- Data is aggregated and contains no sensitive information

Sentiment labels are defined independently from monetary policy stance (e.g. hawkish/dovish), following the methodological discussion in the paper.

---

## Methodological Notes

- Supervised learning models:  
  **Naïve Bayes, Support Vector Machines, Random Forest**
- Feature extraction via **TF-IDF** with custom tokenization
- Evaluation based on **Precision, Recall, F1, Macro-F1**
- Stratified 80/20 train–test split

Full details are available in the paper.

---

## Data Source

- Publicly available **Bank of Thailand press releases**  
- Annotation via AI-assisted labeling with manual validation

---

## Installation Notes

To reproduce the results in the reference notebook, install the required Python dependencies:

```bash
pip install -r requirements.txt
```

This project additionally requires the following NLTK resources, which are not included in `requirements.txt` and must be downloaded separately:

```bash
python -m nltk.downloader punkt wordnet
```

The analysis was executed using **Python 3.10.13** in a virtual environment
