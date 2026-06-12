# RETINA AI: Student Dropout Risk Prediction

## Overview

This project was developed for the **RETINA AI Hackathon**, where the objective was to predict student dropout risk levels using a multimodal dataset containing academic records, attendance time-series data, and counsellor notes.

The model classifies students into:

- Low Risk (0)
- Medium Risk (1)
- High Risk (2)

---

## Participant Information

**Name:** Pratham Kaushik  
**Branch:** CSE-AIML  
**Year:** First Year  
**Kaggle Username:** prathamkaushikaiml

---

## Dataset

The project utilizes three different data sources:

### Academic Data
- CGPA across semesters
- Backlogs
- Family income
- Parent education
- Scholarship status
- Screen time
- Commute time
- Branch information

### Attendance Data
Weekly attendance records were aggregated into:
- Mean Attendance
- Minimum Attendance
- Maximum Attendance
- Attendance Standard Deviation

### Counsellor Notes
Textual counselling remarks were transformed into:
- Note Length Feature

---

## Methodology

1. Data Cleaning and Missing Value Handling
2. Attendance Feature Engineering
3. Counsellor Note Processing
4. Dataset Merging using `student_id`
5. CatBoost Model Training
6. Validation and Cross Validation

---

## Model

**Algorithm:** CatBoost Classifier

Parameters:
- Iterations: 500
- Depth: 8
- Learning Rate: 0.05
- Loss Function: MultiClass

---

## Results

### Validation Performance

**Macro F1 Score:** 0.6027

### 5-Fold Cross Validation

**Mean Macro F1 Score:** 0.6187

---

## Key Findings

Feature importance analysis revealed that:

- `note_length` was the most influential feature.
- Attendance statistics significantly contributed to performance.
- Family income and parent education also played important roles.

One interesting observation was that longer counsellor notes often corresponded to students facing academic or personal difficulties, making note length a surprisingly strong predictor of dropout risk.

---

## Visualizations

The project includes:

- Workflow Diagram
- Model Architecture Diagram
- Confusion Matrix
- Feature Importance Plot
- Training Logs
- Results Summary

---

## Future Improvements

- TF-IDF based NLP features
- Transformer-based text embeddings
- Ensemble learning approaches
- Advanced multimodal architectures

---

## Project Goal

The aim of this project is to assist educational institutions in identifying at-risk students early and enabling timely interventions to improve student retention and academic success.
