# Object Detection Optimizers

## Project Overview

This project compares the impact of different optimization algorithms on two object detection architectures:

- YOLOv8n (One-Stage Detector)
- Faster R-CNN (Two-Stage Detector)

The objective is to analyze how optimizer choice affects:

- Detection performance (mAP50)
- Training convergence
- Inference speed
- Training time
- Computational efficiency

## Dataset

The experiments were conducted using the Pascal VOC 2012 dataset.

For faster experimentation:

- Training subset: 1000 images
- Validation subset: 200 images

## Optimizers Evaluated

- SGD
- AdamW
- RMSProp

## Experimental Setup

- Framework: PyTorch
- YOLO Implementation: Ultralytics YOLOv8
- Faster R-CNN Implementation: torchvision
- Environment: Google Colab (Tesla T4 GPU)
- Epochs: 3

## Evaluation Metrics

### YOLOv8n

- mAP50
- Training Time
- Inference Speed (FPS)

### Faster R-CNN

- Final Loss
- Training Time
- Inference Speed (FPS)

## Results Summary

### YOLOv8n

| Optimizer | mAP50 |
|------------|--------|
| SGD | 0.6249 |
| AdamW | 0.3417 |
| RMSProp | 0.6282 |

### Main Observations

- RMSProp achieved the best YOLOv8n performance.
- SGD showed stable convergence.
- AdamW underperformed with only 3 training epochs.
- Faster R-CNN required more computation than YOLOv8n.

## Repository Structure

```text
.
├── notebooks/
│   └── Object_Detection_Optimizers.ipynb
├── results/
│   ├── yolo_results.csv
│   ├── fasterrcnn_results.csv
│   └── graphs/
├── report/
│   └── Object_Detection_Optimizers.pdf
└── README.md
```

## Authors

- Marwa Bouzaouit
- Aya Adadi
- Malak Boussetta
- Nora Idouaouzal

Faculty of Sciences Ben M'Sick – Casablanca

Academic Year 2025-2026

## Supervisor

Prof. SADIQ MOUNIR
