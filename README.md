# CS5330 - Lab 3: LEGO Object Detection

## Overview
This project focuses on training a YOLOv8 model for LEGO piece detection using a custom dataset. The model is trained and evaluated on a dataset structured in YOLO format, leveraging Colab for training and inference. The goal is to develop an efficient object detection model that can accurately detect and classify LEGO pieces in images.

## Features
- **Dataset Handling**: Extraction and verification of dataset structure.
- **Model Training**: Training YOLOv8 on a custom LEGO dataset with optimized parameters.
- **Evaluation Metrics**: Calculation of precision, recall, mAP, and F1-score to assess model performance.
- **Visualization**: Display of annotated images and model predictions on test images.

## Lab Materials and Descriptions

### 1. **`results/lego_detector`**
This folder contains the results of the trained YOLOv8 model, including:
- **Model Weights**: The best model weights (`best.pt`) and the final model weights (`last.pt`) saved during training.
- **Training Logs**: Logs and metrics recorded during training, such as loss values, precision, recall, and mAP.
- **Visualizations**: Plots of training and validation metrics (e.g., loss curves, precision-recall curves).

These files are essential for analyzing the model's performance and reproducing the results.

---

### 2. **`dataset_test/`**
This folder contains images for displaying results purpose only. The images for testing purpose are included in dataset_yolo.zip

---

### 3. **`dataset_yolo.zip`**
This is the compressed dataset used for training, validation, and testing. It contains:
- **Training Set**: Images and labels for training the model.
- **Validation Set**: Images and labels for validating the model during training.
- **Test Set**: Images and labels for final evaluation of the model.

The dataset is structured in YOLO format, with separate folders for `images` and `labels` in each split.

---

### 4. **`data_preprocess.ipynb`**
This notebook contains the code for preprocessing the dataset, including:
- **Dataset Splitting**: Dividing the dataset into training (70%), validation (15%), and testing (15%) sets.
- **Annotation Conversion**: Converting annotations to YOLO format if necessary.
- **Dataset Verification**: Checking the dataset for consistency and correctness.

This step ensures that the dataset is ready for training and evaluation.

---

### 5. **`lab3.ipynb`**
This is the main notebook for the lab, containing the following sections:
- **Setup and Utilities**: Setting up the environment, installing dependencies, and defining paths.
- **Dataset Extraction and Validation**: Extracting the dataset and verifying its structure.
- **Sample Images**: Visualizing sample images with annotations to ensure the dataset is correctly labeled.
- **Dataset Configuration and Model Training**: Configuring the dataset and training the YOLOv8 model.
- **Model Evaluation**: Evaluating the model on the validation and test sets using metrics such as precision, recall, mAP, and F1-score.
- **Visualization of Predictions**: Displaying model predictions on test images to qualitatively assess performance.

This notebook provides a step-by-step guide to the entire process, from dataset preparation to model evaluation.

---

### 6. **`result_visualization.ipynb`**
The content in this notebook is the visualization portion separated from lab3.ipynb:
- **Prediction Visualization**: Displaying model predictions on a small portion of images to overview the results.

---


## Key Metrics and Results
- **mAP (mean Average Precision)**: The model achieved a high mAP on both the validation and test sets, indicating strong detection performance.
- **Precision and Recall**: The model demonstrated high precision and recall, suggesting accurate detection of LEGO pieces.
- **F1 Score**: The F1 score, which balances precision and recall, was also high, confirming the model's effectiveness.
