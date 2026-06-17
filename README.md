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
## Dataset Distribution
<img width="5938" height="3534" alt="dataset_distribution" src="https://github.com/user-attachments/assets/8080f8ed-2b0b-47e6-b2b4-f0801051381c" />


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

<img width="2942" height="1166" alt="final_architecture" src="https://github.com/user-attachments/assets/66c4bb9b-f712-4588-9c23-993e1f96f6fb" />



---

## Experimental Results

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

<img width="1786" height="1380" alt="confusion_matrix" src="https://github.com/user-attachments/assets/add3707d-442b-4d35-8188-95467c07ab8d" />


### ROC Curve
<img width="1702" height="1361" alt="roc_curve" src="https://github.com/user-attachments/assets/d38d521d-a66b-40b8-a76e-70ca19ca4a30" />


### Precision Recall Curve

<img width="1770" height="1466" alt="pr_curve" src="https://github.com/user-attachments/assets/65e24b0f-4381-4104-97df-9957fde48de3" />


### GNN Training Loss

<img width="1841" height="1407" alt="gnn_training_loss" src="https://github.com/user-attachments/assets/a7faf74a-8eaa-4096-a92c-6debd6494423" />


### GNN Accuracy

<img width="1389" height="1118" alt="gnn_accuracy" src="https://github.com/user-attachments/assets/2cfed7bb-6e59-4d0a-adb3-964c9b643cdb" />


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
## Conclusion

The proposed Hybrid AE-GNN-RF framework effectively combines
feature compression, graph representation learning, and ensemble
classification for intrusion detection. Experimental results on
CICIDS2017 demonstrate high detection capability with
98% accuracy and 99.8% ROC-AUC.

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

Raja Basfore

B.Tech in Computer Science & Engineering

Assam down town University, India

---

## License

This project is released under the MIT License.
