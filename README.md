# Traffic-flow-Prediction-using-GCN_GNN

This project focuses on **predicting traffic flow** using **Graph Convolutional Networks (GCN)** and **Graph Neural Networks (GNN)**. We leverage publicly available traffic datasets to build spatiotemporal models that capture the complex relationships between traffic sensors over time and space.

## 🚦 Overview

Urban traffic forecasting is a key problem in intelligent transportation systems. Traditional models struggle to handle spatial dependencies across a traffic network. In this project, we address this challenge by:

- Representing road networks as graphs
- Modeling temporal patterns using sequence models (like GRU)
- Capturing spatial dependencies with GCN/GNN layers

---

## 📂 Datasets Used

We use two widely-used benchmark datasets provided by the [California Department of Transportation (Caltrans)](http://pems.dot.ca.gov/):

| Model | Dataset | Nodes | Time Steps | Time Interval |
|-------|---------|-------|-------------|----------------|
| GNN   | [PeMSD4](https://github.com/liyaguang/DCRNN/tree/master/data) | 307   | 13824 (59 days) | 5 minutes |
| GCN   | [PeMSD8](https://github.com/liyaguang/DCRNN/tree/master/data) | 170   | 17856 (69 days) | 5 minutes |

> Both datasets include speed/flow data and pre-computed adjacency matrices.

---

## 🧠 Models

### ✅ GNN Model (on PeMSD4)
- Custom Graph Neural Network with attention and GRU-based temporal module
- Learns spatial dependencies using dynamic edge-based aggregation
- Handles spatiotemporal sequence forecasting (multi-horizon)

### ✅ GCN Model (on PeMSD8)
- Standard Graph Convolutional Network using static adjacency matrix
- Forecasts traffic flow for multiple future time steps
- Simple and effective spatial encoder combined with temporal modeling

---

## 📦 Dependencies

- Python 3.8+
- PyTorch
- NumPy
- Pandas
- scikit-learn
- Matplotlib
- tqdm

