# Adversarial Attacks on ResNet-34 & Transferability to DenseNet-121

**Authors:** Nikhil Arora, Devanshi Bhavsar  
**Course:** Deep Learning (CS-GY 6953 / ECE-GY 7123), Spring 2025  
**Repo:** https://github.com/devanshii09/adversarial-patch-benchmark  

---

## Overview

This project implements and analyzes three white-box adversarial attacks on a pretrained ResNet-34 over 500 images drawn from 100 ImageNet classes (indices 401–500), then measures how those adversarial examples transfer to a DenseNet-121:

1. FGSM (single-step, ε=0.02)  
2. PGD (10 steps, ε=0.02, α=0.004, random start)  
3. L₀ Patch (32×32 patch, pixel-domain ε=0.3)  

We report Top-1/Top-5 accuracies, visualize perturbation histograms and failure cases, and export results for easy tabular and graphical summaries.

---

## Features & Tasks

Task 1: Clean-set evaluation (ResNet-34) + qualitative examples + per-class accuracy  
Task 2: FGSM attack: adversarial set, budget checks, histograms, flipping examples  
Task 3: PGD attack: random starts, budget checks, diagnostics  
Task 4: Patch attack: sparse L₀ perturbation, budget checks, mask visualizations  
Task 5: Transferability: regenerate PGD set for DenseNet-121, evaluate all sets, export CSV  
Task 6: Summaries: consolidated CSV (results_summary.csv), grouped bar charts  

---

## Prerequisites

- Python 3.8 or higher  
- PyTorch  
- torchvision  
- numpy  
- pandas  
- matplotlib  
- tqdm  
- Pillow  

If you plan to run on GPU, ensure CUDA is installed and your PyTorch version matches your CUDA toolkit.

---

## Installation

1. Clone the repository:
   git clone https://github.com/devanshii09/adversarial-patch-benchmark.git  
   cd adversarial-patch-benchmark  

2. (Optional) Create a virtual environment:
   python3 -m venv venv  
   source venv/bin/activate       # macOS/Linux  
   venv\Scripts\activate        # Windows  

3. Install dependencies:
   pip install --upgrade pip  
   pip install -r requirements.txt  

---

## Data

Place the 500-image test set under:
data/TestDataSet/  
with subfolders per synset and a labels_list.json file.

Or, on Kaggle, add the dl-3-testdataset via the **Add Data** panel.

---

## Usage

Open the main notebook (main.ipynb) in Jupyter or Kaggle.  
Ensure paths and hyperparameters in the Setup cell point to your data.  
Run cells in order (Task 1 through Task 6).  
Inspect outputs:  
  - CSVs: results_summary.csv, transfer_results.csv  
  - Figures: bar charts, histograms, example grids, patch masks  

---

## Outputs

File: results_summary.csv  
Description: Table of Top-1/Top-5 accuracies for all attacks  

File: transfer_results.csv  
Description: DenseNet-121 transfer results  

---

## Citation

If you use this work, please cite:

@misc{bhavsar2025jailbreaking,  
  title        = {Jailbreaking Deep Models: Adversarial Attacks on ResNet-34 and Transferability to DenseNet-121},  
  author       = {Bhavsar, Devanshi and Arora, Nikhil},  
  year         = {2025},  
  howpublished = {\url{https://github.com/devanshii09/adversarial-patch-benchmark}}  
}  

---

## License

MIT License. See LICENSE for details.
