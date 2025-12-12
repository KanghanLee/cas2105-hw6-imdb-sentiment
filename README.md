# CAS2105 Homework 6 – Mini AI Pipeline Project

## IMDB Sentiment Analysis (Positive / Negative)

**Student:** Kanghan Lee (2024149005)  
**Course:** CAS2105 Computing Research Introduction  
**Model:** DistilBERT (SST-2 fine-tuned)  
**Dataset:** IMDB (200 train / 50 test)

---

## Project Overview

This project implements a small **AI model pipeline** for binary sentiment analysis.
The goal is to compare a simple **naive baseline** with a modern **pre-trained transformer model**
and evaluate their performance on a held-out test set.

The focus of this project is not state-of-the-art performance, but understanding the full AI workflow:
problem definition, baseline design, model selection, evaluation, and reflection.

---

## Methods

### Naive Baseline
- Keyword-based sentiment classification
- Counts occurrences of predefined positive and negative words
- Ignores context and semantic meaning

### AI Pipeline
- Pre-trained transformer model:
  - `distilbert-base-uncased-finetuned-sst-2-english`
- Used for inference only (no fine-tuning)
- Handles contextual and compositional sentiment

---

## Dataset

- **Source:** Hugging Face IMDB dataset
- **Total samples:** 250
- **Train/Test split:** 200 / 50
- **Preprocessing:** Tokenization and truncation handled by the tokenizer

---

## Evaluation Metrics

- Accuracy
- F1-score

---

## Results

| Method | Accuracy | F1-score |
|------|----------|----------|
| Naive Baseline | 0.60 | 0.68 |
| DistilBERT Pipeline | 0.94 | 0.93 |

The transformer-based pipeline significantly outperforms the naive baseline,
especially on reviews with implicit or contextual sentiment.

---

## Files

- `컴연개HW6.ipynb` : Jupyter notebook containing all experiments
- `report.pdf` : Final project report (generated from the Overleaf template)

---

## References

- Sanh et al., *DistilBERT: a distilled version of BERT*, arXiv 2019
- Socher et al., *Recursive Deep Models for Semantic Compositionality*, EMNLP 2013

---

## Notes

This repository is submitted as part of **CAS2105 Homework 6**.
Please refer to `report.pdf` for full experimental details and discussion.
