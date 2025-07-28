# EPFL MNLP Project – STEM AI Tutor

## Objective

The goal of this project was to transform an open-source language model (Qwen3-0.6B-Base) into an **AI tutor specialized in EPFL-level STEM education**. We designed a full post-training pipeline to improve the model’s reasoning ability, factual accuracy, and deployment efficiency.

This was achieved through four major components:
1. **Direct Preference Optimization (DPO)** : to align the model with academic quality preferences,
2. **Supervised Fine-Tuning (SFT)** : to train the model on STEM multiple-choice questions,
3. **Quantization** : to compress the model for efficient inference,
4. **Retrieval-Augmented Generation (RAG)** : to enhance factuality using relevant scientific documents.

## Repository Structure

report.pdf # Our final 6-page report with methods, results and conclusions
description.pdf # Official project instructions provided by the teaching staff
milestone1.zip # Literature review + preference data collection
milestone2.zip # Mid-project deliverables: models, datasets, progress report
milestone3.zip # Final codebase, training scripts, models, RAG documents
