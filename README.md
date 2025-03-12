# CS5330 - Lab 3: LEGO Object Detection

## Overview
This project focuses on training a YOLOv8 model for LEGO piece detection using a custom dataset. The model is trained and evaluated on a dataset structured in YOLO format, leveraging Colab for training and inference. The goal is to develop an efficient object detection model that can accurately detect and classify LEGO pieces in images.

## Features
- **Dataset Handling**: Extraction and verification of dataset structure.
- **Model Training**: Training YOLOv8 on a custom LEGO dataset with optimized parameters.
- **Evaluation Metrics**: Calculation of precision, recall, mAP, and F1-score to assess model performance.
- **Visualization**: Display of annotated images and model predictions on test images.

## Lab Materials and Descriptions
1. **Data Preprocessing** (`data_preprocess.ipynb`):  
   - Split the dataset into training (70%), validation (15%), and testing (15%) sets.  
   - Convert annotations to YOLO format if necessary.  
   - Verify the dataset for consistency and correctness.  

2. **Prepare Dataset for Training** (`dataset_yolo.zip`):  
   - This compressed file contains the dataset required for training, validation, and testing.  
   - Separated folders of `images/` and `labels/` are created for each subset.  

3. **Train the Model** (`lab3.ipynb`):  
   - Set up the environment and install dependencies.  
   - Extract and validate the dataset of `dataset_yolo.zip`.
   - Train the YOLOv8 model and monitor performance using loss, precision, recall, and mAP.  
   - Evaluate the trained model on validation and test sets.  
   - The trained model weights will be saved as `best.pt` and `last.pt` in `results/lego_detector/weights`. Training logs and performance metrics are produced as well.  

4. **Dispaly Model Predictions** (`dataset_test/` & `result_visualization.ipynb`):  
   - A small set of images contained in `dataset_test/` is used to produce sample predictions based on our best trained model. Note that `dataset_test/` is not used in testing process.
   - Use `result_visualization.ipynb` to load the trained model and display predictions.  

## Key Metrics and Results
- **mAP (mean Average Precision)**: The model achieved a high mAP on both the validation and test sets, indicating strong detection performance.
- **Precision and Recall**: The model demonstrated high precision and recall, suggesting accurate detection of LEGO pieces.
- **F1 Score**: The F1 score, which balances precision and recall, was also high, confirming the model's effectiveness.
