# Symptrack 🩺

An AI-powered symptom assessment and urgency classification tool built using fine-tuned **ClinicalBERT**. 

## Overview
Emergency departments face growing pressure from overcrowding and non-urgent visits. **Symptrack** is a secure, safety-first Minimum Viable Product (MVP) designed to classify a user’s described symptoms into three triage categories: **Emergency Room**, **Doctor**, or **Self-care**. 

*Note: Symptrack provides triage guidance and does not offer medical diagnoses.*

---

## Key Features
- **Context-Aware Classification:** Utilizes `Bio_ClinicalBERT` to understand clinical terminology and context (avoiding limitations of static word embeddings like GloVe or BioWordVec).
- **Safety-First Mechanism:** Implements a weighted loss to handle class imbalance, alongside a confidence-based threshold (< 0.65) that defaults uncertain predictions to the Emergency Room to prevent missed emergencies.
- **Interactive UI:** Built with **Gradio** for rapid symptom analysis, featuring clear severity color-coding, likelihood breakdown charts, and a persistent emergency access button.

---

## Project Structure
- `Symptrack_Main_ClinicalBERT.ipynb`: The primary Jupyter Notebook containing data preprocessing, model fine-tuning (ClinicalBERT), evaluation, and inference pipeline.
- **Dataset:** Based on the *Symptom2Disease* dataset from Kaggle, mapped to CTAS (Canadian Triage and Acuity Scale) categories.

---

## Model Performance
- **Macro-F1 Score:** 0.979
- **ER Recall:** 0.966 (Prioritizing patient safety by catching real emergencies)

---

## Team (AI Titans - Group 15)
- **Project Management:** Judy Al-zahranie
- **Data Engineering:** Judy Al-zahranie, Budoor Almanea, Roaa Althagafi
- **ML Development:** Deem Al-rashoud, Roaa Althagafi
- **Training, Tuning & Evaluation:** Raghad Al-Amri, Roaa Althagafi
- **UI & Deployment:** Dania Al-shehri

---

## Disclaimer
This project was developed as part of the Samsung Innovation Campus AI Bootcamp (Capstone Project). 
The classification mapping is guideline-informed (based on CTAS) but has not been clinically validated by a licensed physician. For real-world deployment, professional medical validation is required.
