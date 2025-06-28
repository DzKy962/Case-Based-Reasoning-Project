# Case-Based Reasoning for Legal Case Retrieval and Prediction (Persecution)

 202110370311452 - Ahmad Alif Dzaky F.
 202110370311455 - Muhammad Yurdan Asy Shadzili


 This repository contains the implementation of a Case-Based Reasoning (CBR) system for retrieving and predicting legal case outcomes based on court decision documents from the Indonesian Supreme Court (Mahkamah Agung RI). The pipeline consists of five stages: Case Base Building, Case Representation, Case Retrieval, Solution Reuse, and Model Evaluation.


![case-based-reasoning-diagram](https://github.com/user-attachments/assets/a7f21edf-ce12-4eb5-ab76-5285fb79d03a)


## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Pipeline Stages](#pipeline-stages)
  - [Stage 1: Case Base Building](#stage-1-case-base-building)
  - [Stage 2: Case Representation](#stage-2-case-representation)
  - [Stage 3: Case Retrieval](#stage-3-case-retrieval)
  - [Stage 4: Solution Reuse](#stage-4-solution-reuse)
  - [Stage 5: Model Evaluation](#stage-5-model-evaluation)
- [Running the Full Pipeline](#running-the-full-pipeline)
- [Example Commands](#example-commands)
- [Output Files](#output-files)
- [Contributing](#contributing)
- [License](#license)


## Prerequisites

Sebelum menjalankan proyek ini, pastikan Anda memiliki:

- **Python 3.8 atau lebih tinggi**
- **Akses internet** untuk mengunduh dependencies dan melakukan scraping putusan pengadilan
- **Minimal 8GB RAM** untuk pemrosesan embedding BERT
- **Opsional: GPU** untuk mempercepat komputasi embedding menggunakan IndoBERT


## Installation

1. **Clone the Repository:**
```bash
git clone https://github.com/DzKy962/Case-Based-Reasoning-Project.git
cd Case-Based-Reasoning-Project
```
2. **Create a Virtual Environment (recommended):**
```bash  
python -m venv venv
# On Linux/Mac:
source venv/bin/activate
# On Windows:
venv\Scripts\activate
```
3. **install Dependencies: The project requires several Python libraries listed in requirements.txt. Install them using:**
```bash
!pip install -r requirements.txt
```
```bash
pandas
numpy
requests
beautifulsoup4
pdfminer.six
Sastrawi
scikit-learn
transformers
torch
sentence-transformers
faiss-cpu
rank_bm25
matplotlib
```

4. **Download Pre-trained IndoBERT Model**
```bash
from transformers import AutoTokenizer, AutoModel

tokenizer = AutoTokenizer.from_pretrained("indobenchmark/indobert-base-p2")
model = AutoModel.from_pretrained("indobenchmark/indobert-base-p2")
```

**Project Structure**

CBR-Project/
├── data/
│   ├── eval/                # Metrics, queries, failure cases
│   ├── preprocessed/        # cleaned_putusan_hasil.csv
│   ├── processed/           # cases.csv, cases.json, embeddings.json
│   ├── raw/                 # Raw data: CSV, PDF, case_***.txt
│   └── result/              # Predictions
│
├── Tahap 1 – Membangun Case Base.ipynb         # Stage 1
├── Tahap 2 – Case Representation.py            # Stage 2
├── Tahap 3 – Case Retrieval.ipynb              # Stage 3
├── Tahap 4 – Solution Reuse.ipynb              # Stage 4
├── Tahap 5 – Model Evaluation.ipynb            # Stage 5
│
├── logs/
│   └── cleaning.txt
│
├── logs.txt
├── requirements.txt
└── README.md





