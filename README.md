# 🔢 Multiclass Classification on MNIST

## Context

Continuing my Machine Learning journey inspired by Aurélien Géron's work, I built this project to tackle multiclass image classification on the classic **MNIST** dataset (70,000 grayscale images of handwritten digits).

During my exploration phase, I experimented with several diagnostic tools—including binary classifiers, Precision-Recall curves, and ROC curves—to better understand how different metrics and decision thresholds behave. However, to keep this repository clear, readable, and straight to the point, I deliberately streamlined the final notebook to focus on the core end-to-end workflow.

## Results

After splitting the dataset into 60,000 training images and 10,000 test images and standardizing the pixel features, I benchmarked three algorithms using 3-fold cross-validation: **SGD**, **SVM**, and **Random Forest**.

* **Model Selection:** **Random Forest** achieved the best cross-validation accuracy (**94.14%** on a 10,000-image subset), outperforming SVM (92.94%) and SGD (89.67%).
* **Final Evaluation:** Retrained on the full training set, the Random Forest classifier reached **97% overall accuracy** on the 10,000 unseen test images, with F1-scores ranging from **0.96** to **0.99** across all ten digits.

## Key Takeaways

* **Error analysis goes beyond a single score:** Visualizing the confusion matrix showed that the model's mistakes are not random—they occur primarily between visually similar digits, such as **4s and 9s**, **7s and 9s**, and **3s and 5s**.
* **Curating code is part of the workflow:** Testing multiple curves and diagnostics is essential when experimenting, but keeping only the most relevant steps makes a project much easier to read and share.
