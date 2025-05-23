

# 📊 Making Graphs Accessible with Machine Learning

> Project for STEM Accessibility | NU University | ITSC Department

Overview

This project presents a machine learning-based solution* to automatically extract data from common scientific charts, aimed at making STEM content accessible to students with learning differences or disabilities. The system supports **bar graphs, dot plots, line graphs, and scatter plots**, using a pipeline of image processing and classification models.

Developed as part of a challenge by Benetech, this project is designed to be integrated into a web application for real-time accessibility support.



Objectives

* Automate data extraction from bar, dot, line, and scatter charts
* Support accessibility in STEM education for users with disabilities
* Deliver high accuracy and robustness across multiple chart types

---

 Models Used

| Model                 | Accuracy                      | Notes                                                      |
| --------------------- | ----------------------------- | ---------------------------------------------------------- |
|   Random Forest     | 98.25%                        | Fast and robust with HOG features                          |
|   SVM (One-vs-Rest) | 87%                           | Handles class imbalance with RBF kernel                    |
|   CNN               | 99.12% (train) / 98% (test)   | Deep learning-based solution for image data                |
| ResNet50            | 99.26% (train) / 99.43% (val) | Deep residual learning for high-performance classification |

---

Methodology

* Preprocessing:

  * Resize images to 64×128
  * Convert to grayscale
  * Apply Canny edge detection
  * Extract HOG (Histogram of Oriented Gradients) features

* Model Evaluation:

  * Confusion matrices for per-class analysis
  * Accuracy, precision, and recall calculations

* Training Data Split:

  * Random Forest: 70/30
  * SVM: 80/20
  * CNN & ResNet: 80/20 on \~40,000 images

---

Directory Structure

```
📦 graph-accessibility-ml
├── models/                  # Saved models and weights
├── scripts/                 # Training scripts for RF, SVM, CNN, ResNet50
├── data/                    # Preprocessed datasets and sample inputs
├── reports/                 # Evaluation metrics and confusion matrices         
└── README.md


---

Tools & Libraries

* Python (OpenCV, NumPy, Scikit-learn, Matplotlib)
* PyTorch / Keras / TensorFlow (Deep Learning)
* HOG for feature extraction
* SVM (Scikit-learn), CNN, and ResNet50 (PyTorch)


Results Summary

| Model    | Training Acc | Testing Acc |
| -------- | ------------ | ----------- |
| RF       | \~98.25%     | \~98.25%    |
| SVM      | \~83.37%     | \~87.00%    |
| CNN      | \~99.12%     | \~98.00%    |
| ResNet50 | \~99.26%     | \~99.43%    |

 High accuracy was achieved across models, with ResNet50 showing the best generalization on validation data.

---

 Future Enhancements

* Real-time chart parsing in web or mobile platforms
* Expand dataset with more chart styles and layouts
* Integrate text extraction for axis labels and legends (OCR)
* Support for pie charts and area plots

---


