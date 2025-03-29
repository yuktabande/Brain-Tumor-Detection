# Tumor Detection and Staging Model

## Overview
This project focuses on developing a deep learning-based model for tumor detection and staging. The model first predicts whether a tumor is present in a given medical image. If a tumor is detected, it further classifies the tumor stage based on its shape. This project is part of an ongoing research paper.

## Features
- **Binary Classification**: Detects the presence of a tumor.
- **Multiclass Classification**: If a tumor is detected, it categorizes the tumor into different stages based on its morphological characteristics.
- **Automated Preprocessing**: Includes image normalization, noise reduction, and feature extraction.
- **Deep Learning Architecture**: Utilizes Convolutional Neural Networks (CNNs) for feature extraction and classification.

## Dataset
- The dataset consists of medical images labeled with tumor presence and corresponding stage.
- Data augmentation techniques are applied to enhance model generalization.

## Model Architecture
- **Preprocessing**: Image resizing, grayscale conversion, and histogram equalization.
- **Feature Extraction**: Edge detection and shape analysis to assist in stage classification.
- **Classification**: A CNN model that first predicts tumor presence, followed by a second-stage classifier for tumor staging.

## Training Strategy
- **Loss Function**: Binary Cross Entropy for tumor presence prediction, Categorical Cross Entropy for staging.
- **Optimization**: Adam optimizer with learning rate scheduling.
- **Evaluation Metrics**: Accuracy, Precision, Recall, and F1-Score.
- **Cross-validation**: 10-fold cross-validation for robustness.

## Installation
```sh
pip install -r requirements.txt
```

## Usage
```python
python train.py  # Train the model
python predict.py --image path/to/image.jpg  # Run inference
```

## Results
- Achieves high accuracy in detecting tumors.
- Stage classification is based on shape features extracted from medical images.

## Future Work
- Enhancing dataset size for improved generalization.
- Exploring transformer-based architectures for better feature extraction.
- Integrating explainability methods like Grad-CAM for model interpretability.

