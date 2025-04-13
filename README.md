# 🧠 Hate Speech Detection – OLIDv1

This project was part of the *Introduction to NLP* course at **Vrije Universiteit Amsterdam**.  
The goal was to build a classifier to detect **offensive language** in tweets using the **OLIDv1 dataset**, as part of the [OffensEval 2019](https://aclanthology.org/S19-2010.pdf) shared task (Subtask A).

---

## 👨‍💻 What We Did

- Fine-tuned a **BERT** model (`bert-base-cased`) using the [SimpleTransformers](https://github.com/ThilinaRajapakse/simpletransformers) library
- Implemented two **baseline models**: random and majority classifiers
- Conducted **error analysis** using [CheckList](https://github.com/marcotcr/checklist) with:
  - **Typo perturbations**
  - **Negation handling**
  - **Synthetic template examples**
- Explored tokenizer behavior and subword splitting
- Evaluated model robustness and highlighted areas for improvement

---

## 📊 Results

| Model             | Macro F1 | Weighted F1 |
|------------------|----------|-------------|
| Random Baseline  | 0.49     | 0.53        |
| Majority Baseline| 0.42     | 0.56        |
| **Fine-tuned BERT** | **0.56**     | **0.50**        |

- BERT showed clear improvements over both baselines
- However, performance dropped slightly on typo- and negation-modified examples
- Tokenization issues (e.g. splitting of simple words into meaningless subwords) also impacted results

---
