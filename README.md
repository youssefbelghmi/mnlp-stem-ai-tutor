# EPFL MNLP Project – STEM AI Tutor

## Objective

The goal of this project was to transform an open-source language model (Qwen3-0.6B-Base) into an **AI tutor specialized in EPFL-level STEM education**. We designed a full post-training pipeline to improve the model’s reasoning ability, factual accuracy, and deployment efficiency.

This was achieved through four major components:
1. **Direct Preference Optimization (DPO)** : to align the model with academic quality preferences,
2. **Supervised Fine-Tuning (SFT)** : to train the model on STEM multiple-choice questions,
3. **Quantization** : to compress the model for efficient inference,
4. **Retrieval-Augmented Generation (RAG)** : to enhance factuality using relevant scientific documents.

## Repository Structure

report.pdf : The final 6-page report with methods, results and conclusions.
description.pdf : Official project instructions provided by the teaching staff.
milestone1.zip : Literature review and preference data collection.
milestone2.zip : Mid-project deliverables with models, datasets, and progress report.
milestone3.zip : Final codebase, training scripts, models, RAG documents, etc...

## Milestone 1 – Collecting Preference Data

We collected high-quality **preference-labeled response pairs** using ChatGPT to simulate human preferences.  
Deliverables:
- A one-page **literature review** on prompting, DPO, RAG, and RLHF.
- A JSON dataset of manually annotated preference pairs for ~100 STEM questions per member.

This phase taught us:
- Prompt engineering techniques (e.g., CoT, role prompting),
- How to distill quality alignment data from LLMs,
- The importance of subtle preference differences.

## Milestone 2 – Building Generative Reasoning Models

We trained four specialized models, each by one member:

- **DPO Model**: Used the preference pairs to align the LLM with human-preferred answers.
- **MCQA Model**: Fine-tuned on a large curated dataset of STEM multiple-choice questions.
- **Quantized Model**: Compressed the MCQA model to 4-bit using BitsAndBytes for low-resource deployment.
- **RAG Model**: Combined retrieval (FAISS + Wikipedia + DPO-sourced docs) with MCQA to enrich responses.

We also submitted:
- Training datasets on Hugging Face,
- Model checkpoints,
- A progress report explaining experimental setup and metrics.

## Milestone 3 – Final Improvements and Evaluation

Final steps:
- Improved model performance through better data curation and fine-tuning.
- Evaluated all models using **LightEval**, focusing on accuracy, efficiency, and alignment.

Notable results:
- DPO model reached **82%** accuracy on RewardBench.
- MCQA model with rationale support outperformed all other variants.
- Quantized 4-bit NF4 model halved memory usage with <1% loss in accuracy.
- RAG-enhanced models performed best when combining retrieval and rationale prompts.

## Key Takeaways

- **Alignment via DPO** improves not only human preference matching but also downstream task performance.
- **Rationale prompting** enhances MCQA generalization.
- **Quantization** enables deployment on constrained devices without performance loss.
- **RAG systems** effectively enhance factual precision when well-filtered.
