# Physically-Aware Geometrical Deep Learning Framework for Heusler Compounds

Official implementation of **HeuGNet** developed by **SymMatriX Labs**, a physics-informed Graph Neural Network designed for formation energy prediction in Heusler compounds.

This repository accompanies the manuscript:

> **Physically-aware Geometrical Deep Learning Framework for Heusler Compounds**
>
> Submitted to *Journal of Chemical Information and Modeling (JCIM).*

---

# Table of Contents

- Introduction
- Prerequisites
- Dataset
- Installation
- Usage
- Pre-trained Models
- Explainability
- Citation
- License

---

# Introduction

The attached software package represents the **Heusler Graph Network (HeuGNet)**, a physics-informed graph neural network that integrates materials science knowledge with geometric deep learning to predict the formation energy of Heusler compounds.

HeuGNet extends conventional graph neural network architectures by incorporating physically meaningful atomic descriptors alongside geometric message passing, enabling improved predictive performance while preserving scientific interpretability.

The repository contains the implementation corresponding to the manuscript, including the primary Physics-Informed HeuGNet notebook, the explainability workflow, pre-trained model checkpoints, and the processed dataset required for reproducing the reported experiments.

---

# Prerequisites

The implementation was developed using Python together with the PyTorch ecosystem.

Recommended software requirements include:

- Python 3.10+
- PyTorch
- PyTorch Geometric
- NumPy
- Pandas
- Scikit-learn
- Pymatgen
- Matplotlib
- NetworkX
- Jupyter Notebook

A CUDA-enabled GPU is recommended for efficient model training and inference.

---

# Dataset

The dataset used in this study is provided within the repository.

It contains:

- **Heusler_dataset.csv** containing the material information and target formation energies.
- **cif_files/** containing the corresponding crystal structures.
- **graphs_enhanced.pt**, a preprocessed graph dataset generated from the crystal structures and used directly as input to the HeuGNet framework.

The supplied graph dataset eliminates the need for repeated graph construction, enabling direct reproduction of the experiments presented in the accompanying manuscript.

---

# Installation

Clone the repository

```bash
git clone https://github.com/SymMatriX-Labs/HeuGNet.git
```

Move into the project directory

```bash
cd HeuGNet
```

Install the required Python dependencies

```bash
pip install -r requirements.txt
```

---

# Usage

The complete implementation of the proposed framework is available in

```
Notebooks/HeuGNet_PhysicsInformed.ipynb
```

The notebook performs:

- loading the processed graph dataset (`graphs_enhanced.pt`)
- model definition
- training
- validation
- testing
- performance evaluation

---

# Pre-trained Models

Three trained checkpoints used during this study are provided.

| Model | Description |
|-------|-------------|
| Data-Driven GNN | Baseline graph neural network |
| Feature-Transformed GNN | Enhanced feature representation model |
| Physics-Informed HeuGNet | Final proposed model reported in the manuscript |

These checkpoints may be loaded directly for inference or further evaluation without retraining.

---

# Explainability

The repository additionally includes

```
Notebooks/HeuGNet_Explainability.ipynb
```

which contains the explainability workflow used to analyse the predictions of the proposed HeuGNet model and investigate the learned representations reported in the manuscript.

---

# Citation

If you find this repository useful in your research, please cite the accompanying manuscript.

```bibtex
TBD
```

The citation will be updated following publication.

---

# License

This project is released under the **MIT License**.

See the accompanying `LICENSE` file for complete licensing information.
