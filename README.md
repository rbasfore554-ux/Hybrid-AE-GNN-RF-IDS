# Hybrid-AE-GNN-RF-IDS

A Hybrid Autoencoder–Graph Neural Network–Random Forest Framework for Intrusion Detection using the CICIDS2017 Dataset.

---

## Overview

This project presents a hybrid intrusion detection framework that combines deep feature learning, graph-based representation learning, and ensemble machine learning for accurate cyberattack detection.

The proposed architecture integrates:

- Autoencoder (AE) for feature extraction and dimensionality reduction
- Graph Neural Network (GNN) for capturing structural relationships among network traffic flows
- Random Forest (RF) for final attack classification

The framework is evaluated on the CICIDS2017 benchmark intrusion detection dataset and demonstrates strong classification performance.

---

## Dataset

Dataset Used:

- CICIDS2017

The dataset contains both benign and malicious network traffic, including:

- DDoS
- DoS
- Port Scan
- Botnet
- Brute Force
- Web Attacks
- Infiltration

---

## Methodology

### 1. Data Preprocessing

- Missing value handling
- Feature selection
- Normalization
- Train-test splitting

### 2. Autoencoder Feature Learning

The Autoencoder learns compressed latent representations from network traffic data.

Purpose:

- Noise reduction
- Dimensionality reduction
- Improved feature quality

### 3. Graph Construction

Network traffic is transformed into a graph representation where:

- Nodes represent traffic entities
- Edges represent communication relationships

This allows structural information to be incorporated into the learning process.

### 4. Graph Neural Network

The GNN extracts graph-aware embeddings that capture hidden relationships among traffic flows.

Benefits:

- Structural feature extraction
- Improved attack pattern recognition

### 5. Random Forest Classification

The learned features are passed to a Random Forest classifier for final prediction.

Output Classes:

- Normal
- Attack

### 6. Performance Evaluation

Performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

---

## Proposed Architecture

![Architecture](figures/final_architecture.png)

---

## Experimental Results

### Performance Metrics

| Metric | Value |
|----------|----------|
| Accuracy | 98.0% |
| Precision | 92.0% |
| Recall | 99.0% |
| F1-Score | 96.0% |
| ROC-AUC | 99.8% |

---

## Result Visualizations

<img width="1845" height="1231" alt="results_table" src="https://github.com/user-attachments/assets/d3d774a6-1069-4c53-b07a-413e73e5219d" />

### Confusion Matrix

![Confusion Matrix](results/confusion_matrix.png)

### ROC Curve

![ROC Curve](results/roc_curve.png)

### Precision Recall Curve

![PR Curve](results/pr_curve.png)

### GNN Training Loss

![Training Loss](results/gnn_training_loss.png)

### GNN Accuracy

![GNN Accuracy](results/gnn_accuracy.png)

---

## Repository Structure

```text
Hybrid-AE-GNN-RF-IDS
│
├── notebooks/
│   └── hybrid_ae_gnn_rf_ids.ipynb
│
├── models/
│   ├── autoencoder.pth
│   ├── gcn_model.pth
│   └── random_forest.pkl
│
├── figures/
│   └── final_architecture.png
│
├── results/
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── pr_curve.png
│   ├── gnn_training_loss.png
│   ├── gnn_accuracy.png
│   └── results_table.png
│
└── README.md
```

---

## Requirements

Python Libraries:

```bash
numpy
pandas
matplotlib
seaborn
scikit-learn
torch
torch-geometric
networkx
joblib
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Trained Models

The repository includes trained models:

- Autoencoder (.pth)
- Graph Neural Network (.pth)
- Random Forest (.pkl)

These models can be directly loaded for inference and experimentation.

---

## Future Work

Potential improvements include:

- Real-time Intrusion Detection System deployment
- Graph Attention Networks (GAT)
- Transformer-based anomaly detection
- Explainable AI (XAI)
- Automotive CAN Bus Intrusion Detection
- Edge-based IDS deployment

---

## Author

**Raja Basfore**

B.Tech in Computer Science & Engineering

Assam down town University

India

---

## License

This project is released under the MIT License.
