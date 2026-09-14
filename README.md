# Biobytes — Computational Methods in Biology

**A Biosoc Summer Mentorship Project** **Mentors:** Nischay Patel, Sikha Vamsi

------------------------------------------------------------------------

## Overview

Biobytes is a summer mentorship project run under Biosoc to introduce students (mentees) to **machine learning applied to bioinformatics**. Mentees are taken from ML fundamentals through to three applied case studies — **DNA Sequencing**, **Drug Discovery**, and **Diabetes Prediction** — building practical, project-based experience at the intersection of biology and programming.

This repository contains the project proposal, the weekly curriculum notebooks, and the mentee assignments/projects produced during the program.

### Target Audience & Motivation

Students who want to explore ML and its application in bioinformatics, with no prior prerequisites beyond enthusiasm to learn. The program is designed for those who want an in-depth grounding in ML basics (not just surface-level familiarity) before applying it to real biological problems — computational methods are increasingly central to healthcare, genetics, and drug discovery, and this project walks mentees through that pipeline end-to-end via hands-on case studies.

------------------------------------------------------------------------

## Program Structure

|  |  |
|------------------------------------|------------------------------------|
| **Duration** | 7–8 weeks |
| **Workload** | 8–10 hours/week |
| **Sessions** | 3 per week |
| **Prerequisites** | None — enthusiasm to learn and complete the project |
| **Expected mentees** | 15–17 |
| **Mode / Communication** | Online, via WhatsApp |
| **Tech stack** | Python; Pandas, NumPy, Scikit-learn, TensorFlow; GitHub, Google Colab / Jupyter Notebook |

**Evaluation:** Attendance requires attending at least `n-3` of `n` sessions. Weekly assignments are submitted to a shared GitHub/Drive. A **mid-term evaluation** (report/presentation + short viva) and an **end-term evaluation** (final report/presentation + a GitHub repo containing all code and a project description) gate progress through the program.

------------------------------------------------------------------------

## Curriculum Timeline

| Week | Focus |
|------------------------------------|------------------------------------|
| **1** | Introduction to bioinformatics & ML, setting up Colab/Jupyter/Kaggle/Git/GitHub. *Assignment 1: Python warm-up. Assignment 2: short ML assignment.* |
| **2** | Intermediate ML — missing values, categorical variables, pipelines, cross-validation, decision trees, random forests. *Assignment 3: ML short assignment. Assignment 4: case-study report.* |
| **3** | Feature engineering — feature creation, mutual information, k-best features, target encoding, k-means clustering, PCA. *Assignment 5.* |
| **4** | Python libraries & core models — Matplotlib, Seaborn, Pandas, NumPy, linear & logistic regression. *Assignment 6.* **Mid-term evaluation** (report/PPT + QnA) + Diabetes Prediction task introduced. |
| **5** | DNA sequences & biological databases (UniProt, ChEMBL, NCBI); DNA-sequencing model to predict species from a given sequence. *Assignment 7: code submission.* |
| **6** | Fine-tuning & model validation; introduction to the Drug Discovery project and its reference research paper. |
| **7** | Completion of the Drug Discovery model; submission of code + report/PPT for end-term evaluation. |
| **8** *(optional, if time permits)* | Introduction to deep learning & neural networks — loss functions, backpropagation, CNNs. **End-term evaluation** (report/PPT + QnA). |

------------------------------------------------------------------------

## Repository Contents

```         
Biobytes/
├── Project Proposal_Biosoc.pdf     # Full program proposal (this README is derived from it)
├── Assignments/
│   ├── Linear and Logistic Regression/   # Tutorial notebooks + mentee Assignment/ (Ecommerce, advertising, Titanic)
│   ├── Missing Values and Cateogorical Values/  # Assignment notebooks (Titanic train/test)
│   ├── Matplotlib/                 # Lecture + exercise notebooks
│   ├── Seaborn/                    # Distribution/categorical/matrix/grid/regression plot lectures + exercise
│   ├── Clustering and Mutual Information/  # K-means clustering & mutual-information score notebooks (ames.csv)
│   ├── ML_1/                       # Feature-engineering dataset exercise
│   └── Notebooks/                  # Mentee-run Drug Discovery pipeline (coronavirus target), Titanic logistic regression, unsupervised learning
├── Colab Notebooks/
│   ├── Pandas1.ipynb
│   ├── Python_Assignment_1.ipynb
│   ├── Basics of ML                # (Colab export, no .ipynb extension) — pandas/data exploration
│   └── Final_Project               # (Colab export, no .ipynb extension) — applies the GDSC-IITK "Intro to ML" repo
├── DNA Sequencing/
│   ├── human.txt, dog.txt, chimpanzee.txt   # Labelled coding-sequence datasets for gene-family classification
│   └── example_dna.fa              # Sample Ensembl transcript FASTA file
└── Drug Discovery/
    ├── CDD_ML_Part_1..4_Acetylcholinesterase_*.ipynb   # Reference tutorial notebooks (ChEMBL retrieval → EDA → descriptor calculation → Random Forest regression)
    ├── PaDEL-Descriptor/            # Java tool + fingerprint XML configs for molecular descriptor calculation
    ├── Datasets/ & coronavirus/     # Mentee assignment: same pipeline applied to SARS-CoV-2 main-protease bioactivity data
    └── padel.sh                    # Shell script to run PaDEL descriptor calculation
```

### Curriculum Notebooks

The `Assignments/` folder holds the week-by-week ML fundamentals curriculum: handling missing values and categorical variables, linear and logistic regression, Matplotlib/Seaborn visualisation, and clustering with mutual-information-based feature selection — each paired with a hands-on exercise or assignment notebook.

### DNA Sequencing

Mentees work with labelled DNA coding-sequence datasets for **human, dog, and chimpanzee** genes, building a classifier that predicts a gene family/species from its sequence (via sequence encoding, e.g. k-mer counting) — a self-contained introduction to representing biological sequence data numerically for ML.

### Drug Discovery

The `CDD_ML_Part_1–4` notebooks are the reference **Computational Drug Discovery** tutorial series (Chanin Nantasenamat / "Data Professor"), predicting **Acetylcholinesterase inhibitor** bioactivity (pIC50) from ChEMBL data using PaDEL-calculated molecular descriptors and a Random Forest regressor:

1.  **Part 1 — Bioactivity Data:** retrieve and curate bioactivity data from the ChEMBL database.
2.  **Part 2 — Exploratory Data Analysis:** compute Lipinski descriptors, visualise potency classes.
3.  **Part 3 — Descriptor & Dataset Preparation:** compute PubChem fingerprints via PaDEL-Descriptor.
4.  **Part 4 — Regression with Random Forest:** train and evaluate a bioactivity-prediction model.

Mentees then reproduce this same pipeline as their own project on a **coronavirus (SARS-CoV-2 main protease) target**, producing the staged `coronavirus_0X_bioactivity_data_*.csv` datasets (raw → preprocessed → curated → pIC50-classed → PubChem fingerprints) found in `Datasets/` and `coronavirus/`.

### Diabetes Prediction

Introduced at the mid-term stage per the curriculum; dataset/notebooks for this module were not present in this repository snapshot.

------------------------------------------------------------------------

## Tech Stack

- **Language:** Python
- **Libraries/Frameworks:** Pandas, NumPy, Scikit-learn, TensorFlow, Matplotlib, Seaborn
- **Tools:** GitHub, Google Colab / Jupyter Notebook
- **Domain tools:** ChEMBL web-service API, RDKit, PaDEL-Descriptor (molecular fingerprint/descriptor calculation)

------------------------------------------------------------------------

## Program Design Notes (Reducing Mentee Drop-off)

The proposal specifically builds in three measures to keep mentee engagement high:

1.  A **weekly assignment-solving session** (in addition to regular sessions) so doubts get resolved promptly.
2.  **Lighter weekly workload**, giving mentees with a slower ramp-up enough time to build a strong foundation rather than rushing ahead.
3.  A **dedicated feedback/normal-talks session** to maintain a personal connection and surface issues early.

------------------------------------------------------------------------
