# Predictive Analytics for Brain Stroke Using Machine and Deep Learning

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat-square&logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red?style=flat-square&logo=keras)

> **Author:** Pavani Chirumamila [source: 7]
> **Student ID:** 2835085 [source: 7]
> **Institution:** University of East London [source: 28]
> **Supervisor:** Dr. Sotirios Spanogiannopoulos [source: 7, 28]

---

## 📌 Overview

Brain stroke is a critical medical emergency and a leading cause of long-term disability [source: 148, 151]. This research project focuses on automating the detection and classification of stroke types—specifically **Bleeding (Hemorrhagic)** and **Ischemia**—versus **Normal** brain scans using advanced Deep Learning techniques [source: 9, 10, 344].

The study implemented a hybrid approach, comparing a custom architecture against established transfer learning models [source: 13, 360]:

| Model | Accuracy | F1-Score |
|---|---|---|
| Custom CNN | 31.13% | 14.78% |
| MobileNetV2 (Transfer Learning) | 59.50% | 60.22% |
| ResNet50 (Transfer Learning) | 41.32% | 39.62% |
| **Fine-Tuned MobileNetV2** ⭐ | **68.32%** | **67.49%** |

*Note: Results are based on the final performance comparison [source: 946].*

---

## 🗂️ Dataset

* **Source:** Brain Stroke CT Image Dataset (Kaggle) [source: 348, 381].
* **Classes:** `Bleeding`, `Ischemia`, and `Normal` [source: 349, 382].
* **Preprocessing:** Images were resized to $224 \times 224$ and normalized [source: 407, 411].
* **Augmentation:** Techniques including rotation, zooming, and flipping were applied to enhance model generalization [source: 12, 414, 432].
* **Imbalance Handling:** Class weights were utilized to manage the disparity between normal and stroke-affected samples [source: 22, 465].

---

## Models

* **Custom CNN:** A baseline architecture built from scratch using multiple convolution blocks, batch normalization, and dropout [source: 475, 476, 626].
* **ResNet50:** A deep residual network utilized via transfer learning to identify complex patterns while avoiding the vanishing gradient problem [source: 491, 493, 494].
* **MobileNetV2:** A lightweight architecture pre-trained on ImageNet, used for efficient feature extraction [source: 483, 484, 485].
* **Fine-Tuned MobileNetV2:** The top-performing model, achieved by unfreezing the last 30 layers and retraining with a low learning rate ($1e-5$) [source: 651, 652, 653, 940].

---

## 🛠️ Tech Stack

* **Language:** Python [source: 1041]
* **Deep Learning:** TensorFlow, Keras [source: 397, 439]
* **Data Processing:** NumPy, Pandas
* **Visualization:** Matplotlib, Scikit-learn
* **Environment:** Google Colab / Kaggle API [source: 392, 566]

---

## Key Results

* **Transfer Learning Superiority:** Pre-trained models significantly outperformed custom architectures built from scratch [source: 678, 963].
* **Domain Adaptation:** Fine-tuning MobileNetV2 provided the highest accuracy ($68.32\%$), demonstrating that specialized adaptation is vital for medical diagnostics [source: 18, 912, 969].
* **Evaluation:** Models were rigorously tested using Accuracy, Precision, Recall, F1-Score, Confusion Matrices, and ROC-AUC curves [source: 14, 374, 508].

---

## 🎓 Acknowledgements

Special thanks to **Dr. Sotirios Spanogiannopoulos** at the **University of East London** for his expert guidance and support throughout this Master in Artificial Intelligence dissertation [source: 28, 30].
