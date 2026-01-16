# Equality and Improvement in Mental Health Outcomes  
### An Unsupervised Analysis of Patient-Reported Outcomes in East London

## Project Overview
This project investigates whether mental health treatment outcomes are experienced equally across different demographic groups in East London. Using anonymised patient-reported outcome data collected through the DIALOG tool, the study examines changes in satisfaction across multiple life and treatment domains before and after clinical intervention.

The analysis combines statistical testing and unsupervised machine learning techniques to identify patterns in recovery trajectories and explore potential inequalities related to gender, ethnicity, age, socioeconomic deprivation, and clinical complexity.

This work was completed as part of the MSc in Applied Statistics and Data Science at Queen Mary University of London.

---

## Research Questions
- Do patients show significant improvement in mental health and life satisfaction after treatment?
- Are treatment outcomes experienced equally across gender and ethnic groups?
- Can unsupervised clustering reveal meaningful subgroups of patient experience?
- How do socioeconomic deprivation (IMD), age, and CPA status relate to outcome patterns?

---

## Dataset Description
- **Source:** East London NHS Foundation Trust (ELFT)
- **Tool:** DIALOG – a validated patient-reported outcome measure
- **Sample size:** 6,281 anonymised patient records
- **Structure:** Longitudinal (paired pre- and post-treatment assessments)
- **Domains:**  
  Mental Health, Physical Health, Job Situation, Accommodation, Leisure Activities,  
  Relationships, Friendships, Personal Safety
- **Scale:** 7-point Likert scale (1 = Very dissatisfied, 7 = Very satisfied)

Due to ethical and governance restrictions, the raw data cannot be shared publicly.

---

## Methodology

### 1. Data Preparation
- Included only patients with both pre- and post-treatment assessments
- Derived change scores for each domain
- Categorised IMD deciles into deprivation bands
- No imputation applied to demographic variables (complete-case analysis)

### 2. Statistical Analysis
- Paired t-tests to assess pre/post treatment improvement
- Kruskal–Wallis tests for group-level differences
- Chi-square tests for demographic distribution across clusters

### 3. Unsupervised Learning
Multiple clustering approaches were applied and compared:
- **K-Means Clustering** (Elbow & Silhouette selection)
- **Gaussian Mixture Models (GMM)** using BIC-based model selection
- **Hierarchical Clustering** with Ward’s linkage

Clustering was performed using:
- Pre-treatment scores
- Post-treatment scores
- Combined scores
- Scores augmented with demographic variables

### 4. Visualisation
- Correlation heatmaps (baseline and change scores)
- PCA-based 2D and 3D cluster visualisations
- Cluster composition plots by gender, ethnicity, IMD band, age group, and CPA status

---

## Key Findings
- Statistically significant improvement was observed across all DIALOG domains post-treatment.
- Improvement magnitude varied by domain and demographic group.
- Female patients showed greater average improvement in most domains despite lower baseline scores.
- Ethnic groups differed in baseline satisfaction and recovery patterns, particularly in mental and physical health.
- Socioeconomic deprivation was associated with differential improvement, especially in clinically sensitive domains.
- Clustering revealed overlapping patient profiles, suggesting recovery experiences are continuous rather than neatly separable.

---

## Practical Implications
- Evidence supports the need for more personalised, equity-focused mental health care.
- Recovery should be evaluated across multiple life domains, not just symptom reduction.
- Unsupervised methods can complement traditional audits by uncovering nuanced patient experience patterns.

---

## Tools & Technologies
- **Language:** R
- **Libraries:** tidyverse, mclust, ggplot2, plotly, factoextra, cluster
- **Techniques:** Unsupervised learning, statistical testing, dimensionality reduction

---

## Ethical Considerations
All data used in this project was fully anonymised and accessed under appropriate NHS governance approvals. No identifiable patient information is included in this repository.

---

## Author
**Divya G. Kothari**  
MSc Applied Statistics and Data Science  
Queen Mary University of London
