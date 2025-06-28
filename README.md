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

