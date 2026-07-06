# 🚀 Object Detection Optimizers

A comparative study of optimization algorithms for **YOLOv8n** and **Faster R-CNN** object detection models on the Pascal VOC 2012 dataset.

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red)
![YOLOv8](https://img.shields.io/badge/YOLO-v8-green)
![Torchvision](https://img.shields.io/badge/FasterRCNN-Torchvision-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📖 Overview

This project investigates how different optimization algorithms influence the performance of two major object detection architectures:

- **YOLOv8n** (One-stage detector)
- **Faster R-CNN** (Two-stage detector)

The objective is to determine whether optimizer selection significantly affects:

- Detection accuracy
- Convergence speed
- Loss stability
- Training time
- Inference speed
- GPU memory consumption
- Model robustness

Experiments were conducted using the **Pascal VOC 2012** dataset under identical training conditions to ensure a fair comparison.

---

## 🎯 Objectives

- Compare one-stage and two-stage object detectors.
- Evaluate the influence of different optimizers.
- Analyze training dynamics.
- Compare computational efficiency.
- Study robustness under image perturbations.

---

## 🧠 Models

### YOLOv8n

- One-stage detector
- Real-time inference
- Lightweight architecture
- Implemented using **Ultralytics**

Optimizers:

- SGD
- AdamW
- RMSProp
- NAdam

---

### Faster R-CNN

- Two-stage detector
- Region Proposal Network (RPN)
- High detection accuracy
- Implemented using **Torchvision**

Optimizers:

- SGD
- AdamW
- RMSProp
- Ranger

---

## 📂 Dataset

**Pascal VOC 2012**

- 20 object categories
- Bounding box annotations
- Training / Validation split

YOLO uses converted YOLO annotations, while Faster R-CNN directly uses Pascal VOC XML annotations.

---

## ⚙️ Experimental Setup

Environment:

- Google Colab
- NVIDIA Tesla T4 GPU
- Python
- PyTorch
- Torchvision
- Ultralytics YOLOv8

Training configuration:

- Same dataset split
- Same number of epochs
- Same augmentation
- Same evaluation metrics
- Only the optimizer changes

---

## 📊 Evaluation Metrics

The following metrics are evaluated:

- mAP@0.5
- mAP@0.5:0.95
- Precision
- Recall
- Loss
- Training time
- Inference speed (FPS)
- GPU memory usage
- Robustness to Gaussian noise

---

# 📈 Main Results

## YOLOv8n

| Optimizer | mAP@0.5 |
|-----------|---------|
| SGD | **0.625** |
| RMSProp | **0.628** |
| AdamW | 0.342 |
| NAdam | 0.399 |

Observations:

- RMSProp achieved the best mAP.
- SGD produced very similar performance.
- AdamW and NAdam converged more slowly.
- Inference speed reached approximately **100 FPS**.

---

## Faster R-CNN

| Optimizer | mAP@0.5 |
|-----------|---------|
| Ranger | **0.626** |
| SGD | 0.595 |
| AdamW | 0.522 |
| RMSProp | 0.348 |

Observations:

- Ranger obtained the best accuracy.
- SGD remained highly competitive.
- RMSProp performed worst.
- Average inference speed was approximately **6 FPS**.

---

# 📊 Global Comparison

| Criterion | YOLOv8n | Faster R-CNN |
|------------|----------|--------------|
| Speed | ⭐⭐⭐⭐⭐ | ⭐⭐ |
| Accuracy | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| GPU Memory | ~870 MB | 11–13 GB |
| FPS | 90–100 | ~6 |
| Real-Time | ✅ | ❌ |

---

## 📌 Conclusions

The experiments demonstrate that:

- Optimizer performance depends on the detector architecture.
- SGD is the most consistent optimizer across both models.
- RMSProp performs very well on YOLOv8n.
- Ranger is the best optimizer for Faster R-CNN.
- YOLOv8n is ideal for real-time applications.
- Faster R-CNN is preferable when maximum detection accuracy is required.

---

## 📁 Project Structure

```
Object_Detection_Optimizers/
│
├── yolo/
│   ├── train.py
│   ├── evaluate.py
│   └── configs/
│
├── faster_rcnn/
│   ├── train.py
│   ├── evaluate.py
│   └── optimizers.py
│
├── dataset/
│
├── results/
│   ├── figures/
│   ├── tables/
│   └── logs/
│
├── report/
│   └── Object_Detection_Optimizers_Report.pdf
│
├── requirements.txt
└── README.md
```

---

## ▶️ Installation

Clone the repository

```bash
git clone https://github.com/marwa36maro/Object_Detection_Optimizers.git

cd Object_Detection_Optimizers
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Train YOLOv8

```bash
python yolo/train.py
```

---

## ▶️ Train Faster R-CNN

```bash
python faster_rcnn/train.py
```

---

## 📚 Technologies Used

- Python
- PyTorch
- Torchvision
- Ultralytics YOLOv8
- OpenCV
- NumPy
- Matplotlib
- Google Colab

---

## 👩‍💻 Authors

- **Marwa Bouzaouit**
- Aya Adadi
- Malak Boussetta
- Nora Idouaouzal

Faculty of Sciences Ben M'Sick  
Master of Artificial Intelligence  
Academic Year 2025–2026

---

## 📄 Report

The complete project report is available in the repository.

---

## ⭐ Repository

If you find this project useful, don't forget to ⭐ the repository!
