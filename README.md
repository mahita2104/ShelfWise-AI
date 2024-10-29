# 🛒 ShelfWise-AI

Introducing **ShelfWise-AI**, a groundbreaking AI-driven quality control system designed to transform e-commerce logistics. Developed by **Team No More Panoti**, our solution tackles a critical challenge in the retail sector—ensuring the quality and safety of products, especially in the fast-moving consumer goods (FMCG) and fresh produce categories.

In today’s competitive market, maintaining product quality is paramount. ShelfWise-AI harnesses the power of advanced computer vision and deep learning to automate the inspection process, providing real-time analysis and insights. Our system identifies product defects, verifies expiry dates, and assesses freshness, ensuring that only the highest quality items reach the consumers.

By seamlessly integrating into existing supply chain operations, ShelfWise-AI enhances operational efficiency and boosts customer satisfaction. With our innovative approach, we aim to not only streamline logistics but also promote a more sustainable and reliable e-commerce ecosystem.

Join us as we redefine quality control in the e-commerce industry and create a safer shopping experience for consumers everywhere!


## 🌟 Team Members
- **Mahita Boyina**
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

![Packaging Label Extraction Diagram](Images/Schematic_d1.png)

This module processes an input test image to detect and extract packaging label details. After grayscale conversion and contrast adjustments, Roboflow's object detection model locates key elements such as brand names and weights. The EasyOCR module reads the text from the cropped bounding box, and a Python script identifies and standardizes the brand name.

**Output:** Brand Name

### 2. Expiry Date Validation

![Expiry Date Validation Diagram](Images/Schematic_d2.png)

This module identifies expiry and manufacturing dates along with the MRP by processing an input test image. After grayscale conversion and contrast adjustments, Roboflow’s object detection model locates relevant text on the packaging. EasyOCR reads the text from the cropped image, and a Python script identifies and standardizes dates for uniformity.

**Output:** Expiry Date, Manufacturing Date, MRP

### 3. Freshness Prediction of Produce

![Freshness Prediction Diagram](Images/Schematic_d3.png)

In this module, the input image undergoes resizing and normalization. MobileNetV2, pre-trained on ImageNet and fine-tuned for freshness detection, extracts features to predict the freshness index. Based on predefined thresholds, the system classifies produce into three categories: fresh, medium fresh, and rotten.

**Output:** Freshness Index

---

## 🚀 Technologies at a Glance

- **Object Detection**: **Roboflow 3.0** uses the YOLOv8 architecture, a lightweight convolutional neural network (CNN) designed for high-speed, accurate detection. YOLOv8’s backbone and efficient attention layers allow real-time localization.

- **Optical Character Recognition (OCR)**: **EasyOCR** leverages a CRNN (Convolutional Recurrent Neural Network) combining convolutional layers for feature extraction and bidirectional LSTM layers for sequential text recognition, enabling high-accuracy OCR across complex layouts.
  
![Model-Architecture](Images/EasyOCR-model-architecture.png)
- **Freshness Detection Model**: **MobileNetV2** with transfer learning, focusing on lightweight depthwise separable convolutions to assess freshness based on color and texture.
<p align="center">
  <img src="Images/freshness-detection-model-architecture.png" />
</p> 

---

## 📊 Evaluation Metrics

Below are the performance metrics for each module in the ShelfWise-AI project, showcasing the accuracy and precision of our models in detecting freshness, reading package labels, and validating expiry dates.

- **Reading Package Label**
  - **Mean Average Precision (mAP)**: 79.5%
  - **Precision**: 85.3%
  - **Recall**: 70.5%

- **Expiry Date Validation**
  - **Mean Average Precision (mAP)**: 80.3%
  - **Precision**: 88.0%
  - **Recall**: 74.4%
    
- **Detecting Freshness in Fresh Produce**
  - **Training Precision**: 0.97 (Fresh), 1.00 (Rotten)
  - **Training Recall**: 0.99 (Fresh), 0.97 (Rotten)
  - **Validation Precision**: 0.94 (Fresh), 1.00 (Rotten)
  - **Validation Recall**: 1.00 (Fresh), 0.94 (Rotten)
  - **Overall Accuracy**: 97%


---

## 🖼️ Output Preview

Here’s a preview of the output generated by ShelfWise-AI, demonstrating each module's functionality.

- Brand detection from input test image
  
![Output - Brand Detection](Images/Output1.png)

- Expiry date, manufacturing date, and MRP extraction
  
![Output - Expiry Date Validation](Images/Output2.png)

- Freshness detection for fruits and vegetables

![Output - Freshness Detection](Images/Output3.png)


## 🎥 Demo Video

For a full demonstration of ShelfWise-AI in action, watch the video below:

[Watch the ShelfWise-AI Demo](https://github.com/mahita2104/ShelfWise-AI/raw/main/video.mp4)


