# Project 3: Adversarial Attacks

**Authors:** Nikhil Arora, Devanshi Bhavsar  
**Course:** Deep Learning CS-GY 6953 / ECE-GY 7123 – Spring 2025

## Overview

This Jupyter notebook implements and evaluates adversarial attacks on pretrained image classifiers:

- **Task 1:** Baseline evaluation on clean test set (ResNet-34, DenseNet-121)  
- **Task 2:** FGSM attack generation and analysis (Top-1/Top-5 accuracy, noise histogram, qualitative examples)  
- **Task 3:** PGD attack with random starts & diagnostics (accuracy and CSV export)  
- **Task 4:** Summary table consolidation of all results (Top-1/Top-5)  
- **Task 5:** Visualization via grouped bar charts across models and attacks  

## Requirements

- Python 3.8 or higher  
- PyTorch  
- torchvision  
- numpy  
- pandas  
- matplotlib  

Install dependencies with:

```bash
pip install torch torchvision numpy pandas matplotlib
```

## Setup & Usage

1. Clone the repository and create a virtual environment:

    ```bash
    git clone https://github.com/devanshii09/adversarial-patch-benchmark.git
    cd adversarial-patch-benchmark
    python3 -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt
    ```

2. Place your test images (e.g., an ImageNet subset) in `data/images/`.

3. Open and run the notebook:

    ```bash
    jupyter notebook main.ipynb
    ```

4. Adjust hyperparameters and paths in the **Setup & Configuration** cell as needed.
