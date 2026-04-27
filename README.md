# A Physics-Aware Deep Learning Framework for Heterogeneous Ultrasound Image Classification

## Overview
This repository accompanies the paper:

**"A Physics-Aware Deep Learning Framework for Heterogeneous Ultrasound Image Classification"**  
Published in *Smart Health (2026)*

### Authors
- Enam Ahmed Taufik (European University of Bangladesh)  
- Antara Firoz Parsa (BRAC University)  
- Abdullah Khondoker (BRAC University)  
- Jia Uddin (Endicott College; Woosong University)


## Summary
Classification of medical ultrasound images is challenging due to heterogeneous imaging conditions, device variability, and subtle tissue features. This work proposes a framework that combines Physics-Informed Neural Networks (PINNs) with physics-consistent data augmentation to improve accuracy, robustness, and generalization.

Experiments were conducted on:
- A multi-domain liver fibrosis dataset (6,343 images; five and three-class tasks)  
- A merged breast cancer dataset (1,719 images; benign, malignant, normal)

Images were standardized to 224×224 grayscale. The framework integrates:
- Classical Image Augmentation (CIA) for geometric variability  
- Physics-Informed Augmentation (PIA) to simulate ultrasound-specific artifacts  

Results demonstrate significant improvements in accuracy, F1-score, and convergence speed. The proposed method achieves up to **0.98 accuracy** with **64% fewer training epochs**.


## Key Contributions
- Introduces a **physics-aware deep learning framework** for ultrasound image classification  
- Combines **PINN-based loss functions** with **physics-consistent augmentation (PIA)**  
- Demonstrates improved **generalization across heterogeneous datasets**  
- Achieves significant gains in **accuracy and convergence efficiency**  
- Provides **interpretable feature representations** validated via t-SNE analysis  

---

## Methodology

### Model Overview
The framework integrates:
- CNN backbones: **VGG16, ResNet50, EfficientNetB0**
- Physics-Informed Neural Network (PINN) regularization
- Dual augmentation strategy:
  - **CIA** (flip, rotation, scaling)
  - **PIA** (ultrasound artifact simulation)

### Key Idea
Instead of relying solely on data-driven learning, the model embeds **ultrasound physics constraints** into training. This improves robustness against:
- Device variability  
- Noise and artifacts  
- Domain shifts  


## Setup Instructions

### Requirements
- Python 3.8+
- PyTorch or TensorFlow  
- NumPy  
- OpenCV  
- scikit-learn  
- matplotlib  

### Installation
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
pip install -r requirements.txt


### Data Preparation
1. Resize all images to 224×224 grayscale
2. Organize datasets as:
/data
   /liver
   /breast

## Results

### Performance Comparison

| Dataset | Baseline Accuracy | PINN Accuracy | Improvement | p-value | Cohen's d |
|--------|------------------|--------------|------------|---------|-----------|
| Liver  | 0.87 ± 0.07       | 0.97 ± 0.01   | +10.00%    | 0.16    | 2.18      |
| Breast | 0.63 ± 0.08       | 0.80 ± 0.03   | +16.00%    | 0.16    | 2.85      |

### Key Findings
- PINN improves both **accuracy** and **model stability**  
- Faster convergence (**up to 64% fewer epochs**)  
- More compact and discriminative feature embeddings (**t-SNE analysis**)  

---

## Dataset
- https://ieeexplore.ieee.org/document/  
- https://pubmed.ncbi.nlm.nih.gov/39647406/  
- https://www.sciencedirect.com/science/article/pii/S0010482522011465  
- https://www.cancerimagingarchive.net/collection/breast-lesions-usg/  

---

## Citation
*To be updated*

---

## License

This project is licensed under the **MIT License**.

MIT License

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files...

### Contact

For questions or collaborations:

Enam Ahmed Taufik
Email: enam.ahmed.taufik@gmail.com
