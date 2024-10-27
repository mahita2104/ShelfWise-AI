# 🛒 ShelfWise-AI

**ShelfWise-AI** is an intelligent, AI-driven quality control system designed to streamline e-commerce logistics by ensuring product quality at every step. Developed by **Team No More Panoti** from **Indira Gandhi Delhi Technical University for Women (IGDTUW)**, this project specializes in FMCG and fresh produce inspection through the power of computer vision and deep learning. 

## 🌟 Team Members
- **Mahita Boyina** (Team Leader)
- **Anamika Kumari**
- **Avni Goyal**

---

## 💡 Project Overview

ShelfWise-AI tackles critical challenges in quality assurance for e-commerce and retail logistics. Here’s how it works:

1. **📦 Packaging Label Extraction**  
   Extracts essential information (like brand name and net weight) from product packaging to ensure accuracy and compliance.

2. **📅 Expiry Date Validation**  
   Identifies and standardizes expiry dates, manufacturing dates, and MRP on packaging to maintain up-to-date product information.

3. **🍎 Freshness Prediction of Produce**  
   Assesses the freshness of fruits and vegetables, classifying them as fresh, medium fresh, or rotten based on visual analysis.

---
## 🛠️ Schematic Diagrams

Each component of ShelfWise-AI is represented in the schematic diagrams below. These diagrams provide an overview of the three main functions: packaging label extraction, expiry date validation, and freshness prediction.

### 1. Packaging Label Extraction

![Packaging Label Extraction Diagram](Schematic_d1.png)

This module processes an input test image to detect and extract packaging label details. After grayscale conversion and contrast adjustments, Roboflow's object detection model locates key elements such as brand names and weights. The EasyOCR module reads the text from the cropped bounding box, and a Python script identifies and standardizes the brand name.

**Output:** Brand Name

### 2. Expiry Date Validation

![Expiry Date Validation Diagram](Schematic_d2.png)

This module identifies expiry and manufacturing dates along with the MRP by processing an input test image. After grayscale conversion and contrast adjustments, Roboflow’s object detection model locates relevant text on the packaging. EasyOCR reads the text from the cropped image, and a Python script identifies and standardizes dates for uniformity.

**Output:** Expiry Date, Manufacturing Date, MRP

### 3. Freshness Prediction of Produce

![Freshness Prediction Diagram](Schematic_d3.png)

In this module, the input image undergoes resizing and normalization. MobileNetV2, pre-trained on ImageNet and fine-tuned for freshness detection, extracts features to predict the freshness index. Based on predefined thresholds, the system classifies produce into three categories: fresh, medium fresh, and rotten.

**Output:** Freshness Index

---

## 🚀 Technologies at a Glance

- **Object Detection**: Roboflow 3.0, trained for precise object localization
- **OCR**: EasyOCR for high-accuracy text extraction
- **Deep Learning Model for Freshness**: MobileNetV2 with transfer learning for freshness assessment

---
