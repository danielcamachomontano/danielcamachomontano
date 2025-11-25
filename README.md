# Daniel Camacho Montaño – Master’s Thesis: RAG for Clinical Guidelines

## 📖 Overview

This repository contains the **Master’s Thesis (TFM)** of **Daniel Camacho Montaño**, focused on developing a **Retrieval-Augmented Generation (RAG)** system applied to rheumatology clinical guidelines.  

The project presents a chatbot to support rheumatologists by providing context-aware responses based on clinical guidelines.

---

## 🔹 Project 1 Details

- **Title:** Integration of Retrieval-Augmented Generation (RAG) Architecture for Rheumatology Clinical Guidelines  
- **Goal:** Develop a chatbot to assist rheumatologists using a RAG system  
- **Languages & Tools:** Python, LangChain, OpenAI API, ChromaDB, Pandas, SciPy, Matplotlib, Streamlit (optional)  
- **Original Repository:** [DCM_ARQUITECTURA-RAG](https://github.com/dcamacmon/DCM_ARQUITECTURA-RAG)  

---

## 🔹 Repository Structure

TFM_RAG_clinical_guidelines/
├── guias_clinicas/ # Collected clinical guidelines in PDF
├── PARSEO/ # Scripts for parsing, chunking, embeddings, and RAG pipelines
│ ├── GROBID/ # XML files from Grobid parsing
│ ├── GROBID_MOD/ # Cleaned XML files
│ ├── LlamaCloud/ # Markdown files from Grobid
│ ├── LlamaCloud_TAB/ # Cleaned Markdown files
│ ├── CHUNK1000/ # 1000-character chunks with 150 overlap
│ ├── CHUNK500/ # 500-character chunks with 75 overlap
│ ├── preprocessing.py # Full preprocessing workflow
│ ├── Cargar_vectorstore.py
│ ├── RAG_RERANKER_MEMORY_LANGSMITH_1000.py
│ ├── RAG_RERANKER_MEMORY_LANGSMITH_500.py
│ ├── RAG_sin_Retrieval.py
│ ├── Generación de preguntas.py
│ ├── Generación de respuestas.py
│ ├── ComparaciónRAG500_vs_Generative.py
│ ├── ComparaciónRAG500_RAG1000_Generative.py
│ ├── GRADIO.py
│ ├── Metadata.xlsx
│ └── Evaluación de los modelos.ipynb
├── docs/ # Generated results and evaluations
├── .env # Environment variables for API keys
└── README.md # This file


---

## 🔹 Technologies & Tools

- **Languages:** Python 3.11  
- **Libraries & Frameworks:** LangChain, OpenAI API, Pandas, NumPy, SciPy, Matplotlib, Seaborn, Streamlit  
- **Databases & Vector Stores:** ChromaDB, FAISS  
- **Version Control:** Git and GitHub  

---

## 🔹 Project 2 Details

- **Title:** Machine Learning Report – Mushroom Classification  
- **Goal:** Evaluate multiple machine learning models to classify mushrooms based on morphological and contextual attributes.  
- **Languages & Tools:** R, Python, tidyverse, caret, scikit-learn, matplotlib  

### 🧮 Dataset and Preprocessing

- **Dataset:** 10,000 records, 9 variables (cleaned version of the UCI Mushroom Dataset).  
- **Preprocessing Steps:**  
  - Modal imputation for missing values  
  - One-hot encoding for categorical variables  
  - Z-score normalization for continuous variables  
  - Feature selection to reduce redundancy  

### 🔍 Exploratory Analysis

- Variables such as *stem.color*, *gill.color*, and *cap.diameter* showed mixed distributions, with slight negative skewness in continuous features.  
- PCA was applied to continuous variables (*cap.diameter*, *stem.height*, *stem.width*), and the first two components (CP1 and CP2) explained **94.4%** of the total variance.  
- The PCA plot revealed overlapping clusters between edible and poisonous classes, suggesting the need for **non-linear classification models**.

### 🤖 Evaluated Models

| Algorithm | Accuracy | Sensitivity | Specificity | Notes |
|------------|-----------|-------------|--------------|-------|
| **k-NN (k=11)** | 67.08% | 62.27% | 73.43% | Poor performance, low sensitivity |
| **Naive Bayes** | 68.24% | 67.25% | 69.08% | Mediocre results; Laplace smoothing had little effect |
| **ANN (1 dense layer)** | **93.77%** | 86.89% | 92.61% | Excellent balance between precision and generalization |
| **SVM (Radial kernel)** | **93.48%** | 91.18% | 95.42% | Strong non-linear classifier outperforming linear SVM |
| **C5.0 + Boosting** | ~95% | High | High | Robust and interpretable decision trees |
| **Random Forest (ntree=100)** | **98.32%** | **97.55%** | **98.97%** | Best performance overall, minimal OOB error (2.04%) |

### 🧠 Conclusions

- **Best model:** Random Forest, due to its superior accuracy, sensitivity, and specificity.  
- **Other strong models:** ANN (1 dense layer) and SVM (radial kernel), both highly competitive and efficient.  
- **Less suitable:** k-NN and Naive Bayes, due to their poor classification power.  
- **Overall insight:** Ensemble methods (Random Forest, C5.0) provided the most stable and interpretable results, confirming their suitability for high-stakes classification tasks.


---

## 🔹 Project 3 Details

- **Title:** R-Statistical-Modeling in Experimental Data  
- **Goal:** Analyze biomedical and environmental datasets using advanced statistical models, including linear models and linear mixed-effects models, to evaluate the effects of covariates and treatments.  
- **Languages & Tools:** R, ggplot2, lme4, car, dplyr, lmtest, lmerTest  

### 🧪 Dataset and Analysis

1. **Nitrogen Concentration in Rivers**  
   - **Objective:** Evaluate the effect of land cover (agricultural, forest, urban) and precipitation on nitrogen levels in rivers.  
   - **Analysis:** Linear models with and without precipitation adjustment, ANOVA, Tukey post-hoc tests, model diagnostics (linearity, homoscedasticity, independence, normality of residuals).  
   - **Key Findings:**  
     - Forested areas show higher nitrogen concentrations than urban areas.  
     - Precipitation positively influences nitrogen levels.  
     - Model adjustment for precipitation improves explanatory power (\(R^2\) increases from 0.82 to 0.96).  

2. **Bevacizumab Effect on Creatine Levels in Breast Cancer Patients**  
   - **Objective:** Investigate treatment effects on creatine levels over time in a cohort of patients using linear mixed-effects models.  
   - **Analysis:** Models with random intercepts and slopes per patient, comparison of models using REML and ANOVA.  
   - **Key Findings:**  
     - Treatment with bevacizumab reduces creatine levels compared to control.  
     - Random intercepts model is preferred due to minimal variability in slopes and better balance between complexity and fit.  
     - Both time and treatment have statistically significant effects.  

### 📊 Conclusions

- **Statistical Modeling:** Linear models and mixed-effects models effectively capture the influence of covariates and treatments.  
- **Environmental Insights:** Land cover and precipitation are key determinants of nitrogen levels in rivers.  
- **Biomedical Insights:** Bevacizumab treatment significantly reduces creatine levels in breast cancer patients.  
- **Methodological Note:** Proper model selection and diagnostic checks ensure robust inference and interpretation of results.


## 🧬 Project 4 Details

### 📌 Title
**Gene Expression Analysis and Functional Enrichment in a Murine Model of *Staphylococcus aureus* Infection under Linezolid and Vancomycin Treatment**

### 🎯 Goal
To investigate how *Staphylococcus aureus* infection and antibiotic treatments with linezolid and vancomycin affect gene expression in a murine model, and to characterize the biological processes modulated under each experimental condition.

### 🛠️ Languages & Tools
- **Languages:** R  
- **Packages & Libraries:** Bioconductor (affy, limma, clusterProfiler, pvca, arrayQualityMetrics, genefilter), mouse4302.db  
- **Other Tools:** GEOquery for data retrieval, `ExpressionSet` for microarray data management

---

### 📊 Datasets and Analysis

#### 1️⃣ Affymetrix Microarrays GSE38531
- **Objective:** Assess the impact of infection and antibiotic treatments on gene expression in mice.
- **Analysis:** 
  - Random selection of 24 representative samples per experimental group.
  - Creation of an `ExpressionSet` and RMA normalization.
  - Filtering of low-variability probes (top 10% retained).
  - Construction of design and contrast matrices for differential expression analysis using `limma`.
  - Exploratory analysis: PCA, correlation heatmaps, and PVCA to evaluate batch effects.
- **Key Findings:**
  - Differentially expressed genes identified for each contrast (uninfected vs *S. aureus* with/without antibiotics).
  - Functional enrichment (GO) revealed activation of specific immune and metabolic processes:
    - **Untreated:** immune response, wound healing, and liver development.  
    - **Linezolid:** one-carbon metabolic processes.  
    - **Vancomycin:** iron transport, lectin response, and ion transport.

---

### 📈 Results
- Infection triggers specific immune and metabolic responses.
- Linezolid and vancomycin have distinct transcriptomic effects, modulating biological processes differently depending on the antibiotic.
- PCA and PVCA indicate that experimental factors do not fully explain variability, suggesting possible batch effects or complex interactions.

---

### 📝 Conclusions
- The approach effectively characterizes functional changes associated with infection and antibiotic treatment.
- Integrating differential expression and GO enrichment facilitates biological interpretation of transcriptomic data.
- Results provide insights for future studies on molecular mechanisms of antibiotic response in *S. aureus* infections.

## 🧬 Project 5 Details

### Title
**Nf-L and IL-6 as Predictors of Survival and Motor Function in ALS Patients**

### Goal
To investigate the relationship between blood biomarkers and clinical characteristics with functional progression and survival in patients with amyotrophic lateral sclerosis (ALS), identifying key predictors for risk stratification and clinical monitoring.

### Languages & Tools
R, Python, CSV datasets, Logistic Regression, Linear Regression (OLS and Robust), Stepwise Selection, Partial Least Squares (PLS), LASSO Regression, Data Visualization (corrplot, residual diagnostics).

---

## 📊 Datasets and Analysis

### 1. ALS Biomarkers Dataset (`ela_allBiomarkers.csv`)
- **Objective:** Evaluate the predictive value of a biomarker panel (Nf-L, CRP, IL-6) for 36-month survival and baseline functional score (ALSFRS-R).
- **Analysis:** 
  - Logistic regression for survival prediction.
  - Linear regression (OLS and robust) for ALSFRS-R baseline scores.
  - Stepwise selection, PLS, and LASSO to determine key predictors.
  - Residual diagnostics, multicollinearity checks, and outlier detection.
- **Key Findings:** 
  - Elevated Nf-L and IL-6 are associated with lower survival probability.
  - Onset site (bulbar vs spinal) significantly influences prognosis.
  - Nf-L is negatively correlated with ALSFRS-R baseline score; higher levels predict lower functional ability.
  - LASSO regression selects Nf-L and IL-6 as the most informative predictors for ALSFRS-R decline.
  - Robust models confirm stability of predictors even after removing influential outliers.
  
---

## 📈 Key Results & Conclusions

- **Survival Prediction:** Logistic regression achieved moderate accuracy in external validation (`accuracy = 0.727`, `Kappa = 0.455`). IL-6 inclusion significantly improves model fit (`McFadden R² = 0.201`).
- **Functional Status Prediction:** Nf-L and onset site are primary predictors of baseline ALSFRS-R. Stepwise and LASSO models reinforce the predictive importance of these variables.
- **Statistical Insights:** Robust regression and outlier removal improved model stability and adjusted R² from 0.169 to 0.269 for ALSFRS-R prediction.
- **Clinical Relevance:** Nf-L and IL-6 serve as useful biomarkers for ALS prognosis, functional monitoring, and patient stratification. The site of disease onset provides complementary prognostic information.

💡 **Conclusion:** Blood biomarkers Nf-L and IL-6 are critical for understanding ALS progression and survival, supporting their integration into clinical risk assessment and decision-making frameworks.



## 🔹 How to Use This Repository

1. Clone the repository:

```bash
git clone https://github.com/danielcamachomontano/danielcamachomontano.git


## 🔹 How to Use This Repository

1. Clone the repository:

```bash
git clone https://github.com/danielcamachomontano/danielcamachomontano.git
```

2. Install dependencies (per project):

```bash
pip install -r requirements.txt
```

3. Set environment variables (.env) if a project requires API keys.

4. Run scripts or notebooks according to the project folder of interest.

## 🔹 Purpose of This Repository

This repository aims to showcase the skills and experience of Daniel Camacho Montaño in:

- Developing bioinformatics systems

- Integrating AI and RAG technologies with clinical data

- Biomedical data analysis and visualization

- Reproducible project documentation

## 🔹 Contact

- Email: daniel.camacho060@gmail.com

- LinkedIn: [www.linkedin.com/in/daniel-camacho-montano]

- GitHub: danielcamachomontano

