### CNN for Vegetable Image Classification

---

### Introduction

This repository contains a deep learning project that uses a **Convolutional Neural Network (CNN)** to classify images of vegetables. The project focuses on building a robust classification model and analyzing the impact of image resolution and model complexity on performance.

---

### Project Files

* `CNN_vegClassifer.ipynb`: The Jupyter Notebook with the full source code for data preparation, model architecture, training, and evaluation.
* `CNN_vegClassifer_Slides.pdf`: A presentation summarizing the project, its methodology, and key results.
* `CNN_vegClassifer.html`: A static HTML version of the Jupyter Notebook.

---

### Data Preprocessing & Cleaning

The dataset was carefully prepared to ensure high-quality input for the model. Key steps included:
* **Data Cleaning**: Misclassified images, such as carrots in the "Bean" class folder, were identified and removed from the training set to prevent the model from learning incorrect patterns.
* **Directory Consistency**: Folder names in the validation and test datasets were renamed to match the training set, ensuring seamless data loading and evaluation.
* **Grayscale Conversion**: All images were converted to grayscale to reduce computational complexity and allow the model to focus on important structural features like shape and texture.
* **Image Resizing**: The project compared two different input resolutions:
    * **23x23 Pixels**: A lower-resolution dataset was used to explore a more lightweight and efficient model.
    * **101x101 Pixels**: A higher-resolution dataset was used to capture finer details and evaluate the benefit of a more complex model architecture.

---

### Model Architecture

The core of this project is a Convolutional Neural Network (CNN) built with TensorFlow and Keras. The architecture for the 101x101 model, designed for higher-resolution images, was deeper and more complex to effectively utilize the additional visual information.

---

### Results and Comparison

The project's key finding is a comparison of the 23x23 and 101x101 models:
* **Overall Performance**: The **101x101 model** achieved a slightly higher accuracy of **92.6%**, compared to the **92.3%** of the 23x23 model.
* **Consistency**: The 101x101 model showed more consistent per-class accuracy and fewer misclassifications in its confusion matrix. It was better at differentiating between visually similar vegetables like **cucumber vs. bottle gourd**.
* **Challenges**: The 23x23 model, due to its low resolution, struggled more with visually similar classes, such as brinjal vs. cabbage, as finer details were lost.
* **Conclusion**: Both models are effective, but the **101x101 model offers better generalization and robustness** for visually complex classes, while the **23x23 model is a lightweight and efficient alternative** for scenarios where quick inference is a priority. This demonstrates the trade-off between model complexity, input resolution, and performance.
