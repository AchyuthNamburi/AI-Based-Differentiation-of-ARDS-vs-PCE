# AI-Based Differentiation of ARDS vs Pulmonary Edema using Lung Ultrasound
<img width="466" height="370" alt="Screenshot 2026-03-27 at 3 12 28 PM" src="https://github.com/user-attachments/assets/11541dd5-2e55-4297-85a1-71d2b92bd1c4" />

## 🚀 Overview

This project focuses on developing a deep learning-based diagnostic system to differentiate **Acute Respiratory Distress Syndrome (ARDS)** and **Cardiogenic Pulmonary Edema (CPE)** using lung ultrasound (LUS) imaging.

This project is built upon a structured literature review of 14 research papers and addresses a gap in developing a dedicated ARDS vs CPE binary classifier using LUS.

Both conditions present with visually similar ultrasound patterns (B-lines), but require **completely opposite treatments**. Misclassification can lead to incorrect clinical decisions and severe patient outcomes. This project aims to assist clinicians by providing an **automated, accurate, and explainable AI-based diagnostic tool**.

---

## 🧠 Problem Statement

In critical care settings, rapid differentiation between ARDS and CPE is challenging:

* Both exhibit similar LUS patterns (B-lines)
* Human interpretation is subjective and error-prone
* Reported sensitivity of clinical LUS is only ~82–87%

👉 This project addresses this gap by leveraging deep learning to detect **sub-visual patterns** not easily identifiable by human observers.

---

## 🎯 Objectives

* Build a **binary classifier** for ARDS vs CPE using LUS data
* Improve diagnostic accuracy beyond human baseline
* Incorporate **explainability (XAI)** for clinical trust
* Develop a **hybrid ML pipeline** combining classical and deep learning approaches

---

## 🏗️ Methodology

### 1. Data Processing

* Lung ultrasound images/videos collected using standard protocols
* Preprocessing:

  * Resize and normalization
  * Removal of machine-specific overlays
  * Data augmentation (horizontal flip, brightness adjustments)

---

### 2. Feature Engineering (Classical ML Baseline)

* Extract **GLCM (Gray-Level Co-occurrence Matrix)** features:

  * Contrast, Correlation, Energy, Homogeneity, Entropy
* Train classical classifiers (SVM) for baseline comparison

---

### 3. Deep Learning Models

* **CNN Architectures**:

  * ResNet50
  * InceptionV3
  * Xception (transfer learning)
* **Temporal Modeling**:

  * CNN + LSTM for video-based lung sliding analysis

---

### 4. Clinical Feature Learning

The model is trained to implicitly learn clinically validated LUS features:

* Pleural line irregularity
* Heterogeneous vs homogeneous B-line distribution
* Presence of spared areas
* Subpleural consolidations
* Lung sliding dynamics

---

### 5. Explainability (XAI)

* Integrated **Grad-CAM** to visualize model attention
* Ensures predictions align with clinically relevant regions (pleural zone)

---

### 6. Evaluation Metrics

* AUC (Area Under Curve)
* Sensitivity & Specificity
* F1-score

Model performance is compared against **reported human expert baselines**.

---

## 🔬 Key Contributions

* First attempt at a **dedicated binary ARDS vs CPE classifier** using LUS
* Hybrid pipeline combining:

  * Classical ML (GLCM + SVM)
  * Deep Learning (CNN, CNN+LSTM)
* Incorporation of **clinical interpretability via Grad-CAM**
* Focus on **real-world deployment feasibility (bedside AI)**

---

## 🧰 Tech Stack

* Python
* PyTorch / TensorFlow
* OpenCV
* NumPy, SciPy
* Scikit-learn

---

## 📊 Expected Outcomes

* Improved diagnostic accuracy over traditional LUS interpretation
* Reduction in misclassification of ARDS cases
* Explainable predictions for clinical adoption

---

## 🚧 Status

🟡 Ongoing — Model development and experimentation in progress

---

## 📌 Future Work

* Multi-center dataset validation
* Real-time deployment for bedside inference
* Integration with handheld ultrasound devices
* Clinical trials and physician comparison studies

---

## 🤝 Acknowledgment

This project is inspired by recent advancements in medical imaging AI and aims to bridge the gap between **clinical diagnostics and machine learning systems**.

---

## ⭐ If you found this project interesting, consider giving it a star!
