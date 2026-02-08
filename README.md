# Explainable AI for Object Detection under Occlusion in Autonomous Driving

## 📌 Overview

This project focuses on improving object detection robustness under partial occlusion in autonomous driving scenarios. In addition to enhancing detection reliability, the project integrates Explainable AI (XAI) techniques to analyze and validate model decision-making.

The proposed framework, **OcaDETR**, introduces an Occlusion Attention Module (OAM) to enhance visible features and improve detection performance under heavy occlusion.

---

## 🚗 Motivation

Object detectors perform well when objects are fully visible. However, in real-world urban traffic:

- Pedestrians and vehicles are frequently occluded
- Detection confidence drops under partial visibility
- Missed detections may lead to safety risks
- Most models lack interpretability for failure analysis

This project addresses both robustness and explainability in perception systems.

---

## 🎯 Objectives

- Establish baseline object detection performance (YOLO, DETR)
- Quantify performance degradation under occlusion
- Develop an occlusion-aware enhancement module (OcaDETR)
- Evaluate performance on high-occlusion subsets
- Integrate Explainable AI for interpretability validation

---

## 🏗 Proposed System – OcaDETR

The proposed system extends DETR with an **Occlusion Attention Module (OAM)**.

### Feature Gating Mechanism

g = σ(OAM(F))
F' = F ⊙ (0.5 + g)


Where:
- `F` = backbone feature map
- `g` = learned gating map
- `⊙` = element-wise multiplication

This mechanism enhances visible object regions and suppresses background noise.

---

## 🔬 Methodology

1. Dataset preparation (BDD100K → COCO format)
2. Baseline model training (YOLO, DETR)
3. OcaDETR integration and training
4. Evaluation using COCO metrics
5. High-occlusion subset evaluation
6. Explainability analysis (Grad-CAM / Attention maps)

---

## 📊 Models Used

- YOLOv8 (Ultralytics)
- Faster R-CNN
- DETR (Transformer-based detector)
- OcaDETR (Proposed)
- Grad-CAM / Attention Visualization

---

## 📁 Dataset

**BDD100K (Berkeley DeepDrive 100K)**

- Diverse urban driving scenes
- Day / Night / Weather variations
- Converted to COCO format for training
- Occlusion levels categorized (mild, moderate, heavy)

---

## 📈 Evaluation Metrics

- mAP@50
- mAP@50–95
- Precision
- Recall
- High-occlusion recall (≥ 0.6)

---

## 🔍 Explainable AI Integration

- Grad-CAM heatmaps
- Transformer attention visualization
- Patch sensitivity analysis (optional)

These methods help validate model reasoning and ensure safety transparency.

---

## 🧪 Robustness Evaluation

- Performance across occlusion bins
- Crowded traffic scenario testing
- Comparative degradation analysis (CNN vs Transformer)

---

## 🛠 Tools & Frameworks

- Python
- PyTorch
- Ultralytics (YOLO)
- HuggingFace Transformers (DETR)
- pycocotools
- OpenCV
- Matplotlib

---

## 🔁 Reproducibility

- Code version-controlled using Git
- Modular implementation (Dataset / Training / Evaluation / XAI)
- Configurable hyperparameters
- Same validation split across all models

---

## 🚀 Future Work

- Multi-frame temporal modeling
- Sensor fusion (LiDAR + Camera)
- Embedded real-time optimization
- Cross-dataset validation
- Explicit occlusion supervision

---

## 🧠 Key Contribution

This work proposes a reliability-driven detection framework that integrates:

- Occlusion-aware feature modulation
- Robust evaluation under perceptual uncertainty
- Explainable AI validation for safety-critical systems

---

## 📜 License

For academic and research purposes.

---


