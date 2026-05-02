# L2 Writing Error Analysis with LLMs

## Overview
This project explores how large language models (LLMs) can detect and classify errors in second language (L2) writing, with a focus on lexical naturalness, discourse, and meaning rather than traditional grammar-only evaluation.

## Tasks
Task 1 (Error Detection): Given a sentence and a highlighted span, the model predicts whether the span is an actual error.

Task 2 (Error Type Classification): Given a sentence and a known error span, the model classifies the type of error. The labels include Expression (lexical naturalness), Discourse (coherence and structure), and Meaning (clarity and interpretability). This is a multi-label classification task.

## Dataset
The dataset consists of annotated L2 learner sentences with marked error spans.

- Task 1 dataset: used for error vs. non-error prediction  
- Task 2 dataset: used for error type classification (Expression, Discourse, Meaning)

Folder structure:
data/
  ├── task1_full_dataset.csv
  └── task2_full_dataset.csv

## Method
Model: Qwen3-8B

Three prompting conditions are used:
- Zero-shot  
- Few-shot (constructed from labeled examples in the dataset)  
- Human-style prompt (based on annotation guidelines)

## Notebook
All experiments are implemented in:
notebooks/experiment_all_conditions.ipynb

The notebook includes:
- Task 1 (Error Detection)
- Task 2 (Error Type Classification)
- All prompting conditions
- Evaluation pipeline

## How to Run
1. Install dependencies:
pip install -r requirements.txt

2. Open and run:
notebooks/experiment_all_conditions.ipynb

## Paper
The full paper is included in:
paper/

## Notes
- Few-shot examples are dynamically constructed from the dataset
- Prompts are implemented directly in the notebook
