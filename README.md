# Hybrid Semantic Search System

A Hybrid Semantic Question Answering (QA) system that combines **Ontology-based Knowledge Graphs** with **Retrieval-Augmented Generation (RAG)** to improve question answering and course retrieval over a MOOC (Coursera) dataset.

This project demonstrates how symbolic reasoning and neural retrieval can work together to provide more accurate, reliable, and semantically meaningful search results.

---

## 📌 Project Overview

Traditional search systems rely on keyword matching, which often fails to understand user intent. While Retrieval-Augmented Generation (RAG) improves semantic understanding, it may produce inaccurate factual information. Ontology-based systems provide precise factual retrieval but lack semantic flexibility.

To overcome these limitations, we developed a **Hybrid Semantic Search System** that combines the strengths of both approaches.

---

## 🚀 Features

- Ontology-based Knowledge Graph
- RDF Triple Generation
- Semantic Search using Sentence Transformers
- FAISS Vector Database
- Hybrid Fusion Layer
- Metadata Enrichment
- Benchmark Evaluation
- Performance Comparison between Ontology, RAG, and Hybrid models

---

## 🏗️ System Architecture

The system consists of three major components:

### 1. Symbolic Layer (Ontology)

- RDF Knowledge Graph
- Classes:
  - Course
  - Instructor
  - Organization
  - Level
- Object Properties:
  - taughtBy
  - offeredBy
  - hasLevel
- Data Properties:
  - hasDescription
  - hasModules
  - hasCourseIndex

---

### 2. Neural Layer (RAG)

Semantic retrieval is performed using:

- Sentence Transformers
- all-MiniLM-L6-v2
- 384-dimensional embeddings
- FAISS similarity search

---

### 3. Fusion Layer

The Fusion Layer intelligently combines both systems by:

- Routing factual questions to the ontology
- Using semantic retrieval for open-ended questions
- Re-ranking retrieved courses using ontology metadata

---

## 📂 Dataset

Source:

- Coursera Dataset (Hugging Face)

Original Dataset Size:

- ~6,500 courses

Final Clean Dataset:

- **5,827 courses**

Dataset includes:

- Course Title
- Instructor
- Organization
- Difficulty Level
- Course Description
- Module Information

---

## 🧹 Data Preprocessing

The preprocessing pipeline includes:

- Removing duplicate records
- Handling missing values
- URI normalization
- Standardizing difficulty levels
- Synchronizing ontology and RAG datasets

---

## 🧠 Technologies Used

- Python
- RDF
- SPARQL
- rdflib
- Pandas
- Sentence Transformers
- FAISS
- Hugging Face Datasets
- NumPy

---

## 📊 Evaluation

Benchmark:

- **210 Queries**

Query Distribution:

- 150 Factual Queries
- 50 Semantic Queries
- 10 Hybrid Queries

Evaluation Metrics:

- Mean Reciprocal Rank (MRR)
- Recall@5

---

## 📈 Results

| Retrieval System | Overall MRR | Recall@5 |
|-----------------|------------:|----------:|
| Ontology | 0.7619 | 0.7619 |
| RAG | 0.7419 | 0.8619 |
| **Hybrid** | **0.8671** | **0.9190** |

The Hybrid system achieved the best balance between factual accuracy and semantic retrieval.

---

## 📁 Repository Structure

```
├── data/
│   ├── raw_dataset.csv
│   └── cleaned_dataset.csv
│
├── ontology/
│   └── course_ontology.rdf
│
├── notebooks/
│   └── Hybrid_QA_System.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── ontology_builder.py
│   ├── rag_pipeline.py
│   ├── fusion.py
│   ├── evaluation.py
│   └── utils.py
│
├── report/
│   └── Hybrid_Semantic_QA_Report.pdf
│
├── README.md
└── requirements.txt
```

---

## 💡 Future Improvements

- Expand the ontology with skills, topics, and prerequisites
- Integrate Large Language Models (LLMs) for answer generation
- Use Graph Neural Networks (GNNs)
- Apply Knowledge Graph Embeddings
- Support multi-hop reasoning
- Evaluate hallucination and answer completeness

---

## 👥 Authors

- Amro Emad Hassan Askar
- Osama Haider
- Andrea Muscio

---

## 📄 Project Report

The complete report describing the project methodology, architecture, implementation, experiments, and evaluation is included in this repository.

---

## 📜 License

This project was developed for academic purposes as part of a university semester project.

---
## ⭐ Acknowledgements

Special thanks to our instructors and the University of Milano-Bicocca for providing the opportunity to explore Neuro-Symbolic AI, Knowledge Graphs, and Retrieval-Augmented Generation through this project.
