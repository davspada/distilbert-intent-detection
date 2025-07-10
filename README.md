# DistilBERT for Intent Detection on CLINC150 Dataset
Fine-tuning the DistilBERT transformer model on the CLINC150 dataset for the task of intent detection. Intent detection is a core task in natural language understanding (NLU), often used in systems such as chatbots, virtual assistants, and customer support tools.

## Overview

The project involves adapting and fine-tuning the DistilBERT model for multi-class classification, focusing on 150 distinct intents from the CLINC150 dataset. The dataset includes a diverse range of real-world user queries, making it an excellent benchmark for evaluating intent detection models.

### Objectives
1. **Data Preparation:** Load, preprocess, and explore the CLINC150 dataset.
2. **Fine-Tuning:** Train a DistilBERT model for multi-class classification (150 intent classes).
3. **Evaluation:** Measure performance using metrics like accuracy and F1-score, with detailed per-class analysis.
4. **Error Analysis:** Identify model limitations by examining misclassified examples.

---

## Features

- **Dataset:** Includes training, validation, and test splits of the CLINC150 dataset with in-scope and out-of-scope (OOS) intents.
- **Tokenizer:** Utilizes the `DistilBertTokenizerFast` for efficient text preprocessing.
- **Model:** Fine-tunes the `DistilBertForSequenceClassification` model, a lightweight version of BERT optimized for speed and efficiency.
- **Metrics:** Computes accuracy, weighted F1-score, and macro F1-score for balanced evaluation.
- **Training Configuration:** Supports GPU acceleration, logging, and model checkpointing using Hugging Face's Trainer API.

---

## Dataset
The [CLINC150 dataset](https://github.com/clinc/oos-eval) is a benchmark dataset consisting of:

- **150 Intents:** Fine-grained user intents across various domains.
- **Out-of-Scope Examples:** Queries that do not belong to any of the defined intents.
- **Splits:** Training (15,250 examples), validation (3,100 examples), and test (5,500 examples).

## Results

### Metrics
- **Accuracy:** ~95.3% on the validation set.
- **Weighted F1-Score:** ~95.2% on the validation set.
- **Macro F1-Score:** ~95.6% on the validation set.

### Error Analysis
The model performs well across most classes but struggles with:
- Misclassifications between semantically similar intents.
- Handling out-of-scope examples.

---

## Acknowledgements
- [Hugging Face Transformers](https://huggingface.co/transformers/) for model and tokenizer implementations.
- [CLINC150 Dataset](https://github.com/clinc/oos-eval) for providing the dataset.
- [Hugging Face Datasets](https://github.com/huggingface/datasets) for seamless dataset loading.

---
