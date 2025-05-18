# 🛣️ Integrated Object Detection, Road Segmentation, and Path Finding for Autonomous Vehicles with Explainable AI

### 🎓 Amrita Vishwa Vidyapeetham | Artificial Intelligence Engineering

**Team Members**  
- Bhanushray Gupta [CB.EN.U4AIE22009]  
- Gnanasabesan [CB.EN.U4AIE22018]  
- Naga Koushik [CB.EN.U4AIE22046]  
- Praneeth Tvs [CB.EN.U4AIE22054]  

---

## 📌 Overview

This project proposes a modular, explainable pipeline for autonomous vehicles that integrates:

- **Object Detection** (YOLOv10 + Faster R-CNN)  
- **Road Segmentation** (EfficientPS + Mask2Former)  
- **Path Planning** (A* Algorithm with Cubic Spline Smoothing)  
- **Explainable AI** (SHAP & Grad-CAM)

The goal is to enhance safety, transparency, and real-world applicability of autonomous systems.

---

## 🚦 Motivation

Current autonomous driving systems face challenges such as:
- Lack of transparency in decision-making (black-box AI)
- Poor lane detection in curved or discontinuous roads
- Inefficient trajectory planning in complex environments
- Performance drops in object detection under occlusion or low-quality imaging

---

## 📊 Datasets

| Task              | Dataset      | Source                                                                 |
|-------------------|--------------|------------------------------------------------------------------------|
| Object Detection  | KITTI        | [Kaggle: KITTI Dataset](https://www.kaggle.com/datasets/klemenko/kitti-dataset) |
| Road Segmentation | Cityscapes   | [Kaggle: Cityscapes](https://www.kaggle.com/datasets/dansbecker/cityscapes-image-pairs) |

---

## 🔍 Methodology

### 🔹 Perception Module
- **Object Detection:**  
  - YOLOv10 (fast inference) + Faster R-CNN (high accuracy)  
  - Non-Max Suppression with IoU threshold of 0.5  
  - Interpretability: SHAP to visualize influential regions

- **Road Segmentation:**  
  - EfficientPS with multiscale fusion  
  - Mask2Former for transformer-based mask refinement  
  - Grad-CAM for understanding segmentation layers

### 🔹 Planning Module
- A* Algorithm on the drivable mask  
- Dynamic goal selection: Chooses widest road region  
- Cubic Spline Smoothing for real-world drive paths  
- Off-road correction mechanism

### 🔹 Explainability Module
- SHAP for object detection output interpretation  
- Grad-CAM for segmentation heatmaps  

---

## 🧠 Model Summary

| Component           | Model(s)                             | Dataset     | Notes                                 |
|---------------------|--------------------------------------|-------------|----------------------------------------|
| Object Detection    | YOLOv10 + Faster R-CNN (ResNet50)    | KITTI       | Fast + accurate combination            |
| Road Segmentation   | EfficientPS + Mask2Former            | Cityscapes  | Multiscale + Transformer Decoder       |
| Pathfinding         | A* + Cubic Spline Smoothing          | Custom      | Real-time safe pathfinding             |
| Explainability      | SHAP, Grad-CAM                       | Model Outputs | Enhances transparency and trust       |

---

## 🧪 Simulation

- Simple UI with background and car overlay  
- Object boxes as obstacles  
- Real-time path plotted using A*  
- Output: Safe navigable path on road image

---

## ✅ Conclusion

We present a robust, explainable autonomous driving system using:
- State-of-the-art deep learning for perception  
- Classical algorithms for safe planning  
- Explainability to ensure transparency and adoption

This hybrid approach allows high performance, safety, and interpretability—crucial for real-world deployment.

---

## 📚 References

- Explainable Artificial Intelligence for Autonomous Driving  
- Dynamic Lane Segmentation using Neural Networks  
- On-Road Trajectory Planning with Hierarchical Refinement  
- Challenges in Deep Learning-based Object Detection  

---

