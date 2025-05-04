
# 🧠 Object Detection with DETR: ResNet50 vs Vision Transformer

This repository provides an implementation of the **DEtection TRansformer (DETR)** architecture for object detection, comparing two powerful backbones:

* 🌀 **ResNet50**
* 🚀 **Vision Transformer (ViT)**

## 📌 Project Overview

This project implements and evaluates two DETR variants for object detection using the **Pascal VOC 2007** dataset:

1. 🔹 **DETR + ResNet50**
2. 🔸 **DETR + Vision Transformer (ViT)**

Using **PyTorch**, the project explores the effectiveness of transformers in end-to-end object detection.

---

## ✨ Features

* ✅ Implementation of DETR with both **ResNet50** and **ViT** backbones
* 🧾 Data loading + preprocessing for **Pascal VOC 2007**
* 🛠️ Custom training & evaluation pipelines
* 🧮 Hungarian matching for bounding box prediction
* 📊 Comprehensive metrics: `mAP`, `AP50`, `AP75`, `Precision`, `Recall`, `F1`
* 🖼️ Detection result visualizations

---

## 📦 Requirements

* `Python >= 3.6`
* `PyTorch >= 1.7`
* `torchvision`
* `numpy`, `scipy`, `matplotlib`, `tabulate`

---

## 🗃️ Dataset

We use the **Pascal VOC 2007** dataset with 20 object classes (e.g. `person`, `car`, `dog`, `cat`). The dataset is downloaded and preprocessed automatically.

---

## 🧱 Model Architecture

### 🔷 DETR: End-to-End Object Detection

DETR replaces complex pipelines with a **transformer encoder-decoder** model that directly predicts object sets, eliminating the need for:

* Anchors
* Region Proposal Networks (RPN)
* Non-Maximum Suppression (NMS)

### 🏗️ Backbones Compared

* **🌀 ResNet50**: Strong CNN baseline for feature extraction
* **🚀 Vision Transformer (ViT)**: Pure transformer-based model treating images as patch sequences

---

## 📈 Results & Metrics

### 🔍 Quantitative Results


| 🧪 Metric       | ResNet50 DETR | ViT DETR   |
| --------------- | ------------- | ---------- |
| 📏 **mAP**      | 0.9500        | 0.9500     |
| 🎯 **AP50**     | 0.9500        | 0.9500     |
| 🎯 **AP75**     | 0.9500        | 0.9500     |
| ✅ **Precision** | 0.6493        | **0.9820** |
| 📊 **F1 Score** | 0.7873        | **0.9909** |

---

### 🧠 Quick Summary

* **mAP, AP50, AP75**: ⚖️ **Equal** performance
* **Precision**: 🚀 **ViT outperforms** ResNet50
* **F1 Score**: 🚀 **ViT is significantly better**

➡️ **Conclusion**: While both models achieve excellent detection accuracy, the **Vision Transformer** backbone clearly leads in **precision** and **F1 Score**, making it the superior choice for accuracy-focused applications. However, **ResNet50** remains efficient for **resource-constrained** environments.

---

## 🚀 Usage

1. Open the notebook in **Google Colab** or **Jupyter**
2. Run all cells:

   * 📥 Download Pascal VOC
   * 🏋️ Train DETR models
   * 📈 Evaluate performance
   * 🖼️ Visualize predictions

---

## 📚 References & Acknowledgments

This project is inspired by:

* **[DETR Paper: "End-to-End Object Detection with Transformers"](https://arxiv.org/abs/2005.12872)** by Carion et al.
* **[Official DETR GitHub Implementation](https://github.com/facebookresearch/detectron2)**
* PyTorch and torchvision libraries


