# Daniel Camacho Montaño – Master’s Thesis: RAG for Clinical Guidelines

## 📖 Overview

This repository contains the **Master’s Thesis (TFM)** of **Daniel Camacho Montaño**, focused on developing a **Retrieval-Augmented Generation (RAG)** system applied to rheumatology clinical guidelines.  

The project presents a chatbot to support rheumatologists by providing context-aware responses based on clinical guidelines.

---

## 🔹 Project Details

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