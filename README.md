
# Classification of Malignant Melanoma in Canines Using Deep Learning

## Project Overview

This project investigates the application of deep learning to the classification of canine cutaneous tumour histopathology images. It explores how convolutional neural networks and transfer learning architectures can be used to classify tissue regions into five categories, including malignant melanoma.

The project uses histopathological whole-slide images from the CATCH dataset and compares three deep learning architectures:

- Deep Convolutional Neural Network (DCNN)
- VGG16
- EfficientNet-B0

The models were trained and evaluated using image tiles extracted from the histopathology images.

## Project Objectives

- Explore histopathological images of canine cutaneous tumours.
- Develop a deep learning model to classify different tissue types.
- Investigate the effect of class imbalance and data augmentation.
- Apply transfer learning using pre-trained VGG16 and EfficientNet-B0 architectures.
- Compare model performance using test accuracy, precision, recall and F1-score.
- Examine the potential of deep learning for supporting histopathological image classification research.

## Dataset

The project uses the CATCH dataset, which contains 350 canine cutaneous tumour haematoxylin and eosin (H&E) whole-slide images.

The dataset includes polygon annotations created using SlideRunner.

Five tissue categories were considered:

| Class | Description |
|---|---|
| Subcutis | Subcutaneous tissue |
| Dermis | Dermal tissue |
| Epidermis | Outer layer of the skin |
| Melanoma | Melanoma tumour tissue |
| Necrosis | Areas of tissue necrosis |

The images were processed into smaller image tiles for model development.

**Image specifications:**
- Image input size: 224 × 224 pixels
- Number of classes: 5
- Batch size: 32
- Label encoding: One-hot encoding

## Methodology

### 1. Data Preparation

The histopathology images were prepared for deep learning classification through image loading, preprocessing and label encoding.

The dataset was divided into training, validation and test subsets using a 70:15:15 split.

### 2. Exploratory Data Analysis

Exploratory analysis was performed to examine the distribution of the five tissue classes and identify class imbalance.

### 3. Addressing Class Imbalance

Different approaches were investigated during model development, including:

- Class weighting
- Synthetic Minority Over-sampling Technique (SMOTE)
- Image data augmentation

These approaches were explored to improve the representation of minority classes during training.

### 4. Model Development

Three architectures were investigated.

**Deep Convolutional Neural Network (DCNN)**

A custom convolutional neural network was developed using convolutional layers, pooling, batch normalisation and other classification layers. Different training configurations were explored, including class weighting, data augmentation and learning-rate adjustments.

**VGG16**

A pre-trained VGG16 architecture was used for feature extraction. The extracted features were passed through additional classification layers. Model tuning included changes to the learning rate and optimisation settings.

**EfficientNet-B0**

EfficientNet-B0, pre-trained on ImageNet, was used for feature extraction. Its pre-trained layers were frozen, and additional classification layers were trained to classify the five tissue categories.

### 5. Model Evaluation

The models were evaluated using a held-out test dataset.

The evaluation metrics included:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrices

## Results

The best recorded test accuracy for each architecture is summarised below.

| Model | Test Accuracy | Test Loss |
|---|---:|---:|
| DCNN | 91.03% | 0.2628 |
| VGG16 | 96.40% | 0.1703 |
| EfficientNet-B0 | 96.20% | 0.1612 |

### Classification Performance

The following tables present the classification metrics from the best recorded experiments in each notebook.

#### DCNN

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Subcutis | 0.97 | 0.98 | 0.98 |
| Dermis | 0.86 | 0.91 | 0.89 |
| Epidermis | 0.93 | 0.86 | 0.89 |
| Melanoma | 0.90 | 0.92 | 0.91 |
| Necrosis | 0.90 | 0.95 | 0.92 |
| **Macro Average** | **0.91** | **0.92** | **0.92** |
| **Weighted Average** | **0.91** | **0.91** | **0.91** |

#### VGG16

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Dermis | 0.95 | 0.96 | 0.95 |
| Epidermis | 0.96 | 0.95 | 0.96 |
| Melanoma | 0.96 | 0.97 | 0.97 |
| Necrosis | 0.98 | 0.97 | 0.98 |
| Subcutis | 0.98 | 0.99 | 0.99 |
| **Macro Average** | **0.97** | **0.97** | **0.97** |
| **Weighted Average** | **0.96** | **0.96** | **0.96** |

#### EfficientNet-B0

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Dermis | 0.97 | 0.95 | 0.96 |
| Epidermis | 0.95 | 0.95 | 0.95 |
| Melanoma | 0.94 | 0.96 | 0.95 |
| Necrosis | 0.98 | 0.98 | 0.98 |
| Subcutis | 0.99 | 0.99 | 0.99 |
| **Macro Average** | **0.97** | **0.97** | **0.97** |
| **Weighted Average** | **0.96** | **0.96** | **0.96** |

### Results Interpretation

VGG16 achieved the highest recorded test accuracy at 96.40%, closely followed by EfficientNet-B0 at 96.20%. The custom DCNN achieved 91.03%.

All three models demonstrated the ability to classify the five tissue categories, although performance varied across individual classes.

VGG16 and EfficientNet-B0 achieved particularly strong classification results across the tissue categories, including melanoma.

The results suggest that transfer learning offered a promising approach for this histopathological image classification task.

**Note:** The models were evaluated using test sets with different class distributions in the respective notebooks. Consequently, the results should be interpreted as the best recorded outcomes from separate experiments, rather than a strictly controlled comparison using an identical test set.

## Tools and Technologies

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- Jupyter Notebook

## Repository Contents

The repository contains the Jupyter notebooks used for:

- Custom DCNN development and evaluation.
- VGG16 feature extraction, training and tuning.
- EfficientNet-B0 feature extraction, training and tuning.

The original histopathology images and extracted image arrays are not included in the repository.

## Conclusion

This project explored the use of deep learning for classifying canine cutaneous tumour histopathology images.

The experiments demonstrated promising classification performance across five tissue categories. VGG16 achieved the highest recorded test accuracy, followed closely by EfficientNet-B0.

The project provided practical experience in histopathological image processing, convolutional neural networks, transfer learning, class imbalance management, model optimisation and performance evaluation.

The results represent experimental model performance and should not be interpreted as evidence of clinical diagnostic validation.

## References

- CATCH dataset – canine cutaneous tumour histopathology images.
- Keras documentation: https://keras.io/
- TensorFlow documentation: https://www.tensorflow.org/
- Scikit-learn documentation: https://scikit-learn.org/
- EfficientNet: https://keras.io/api/applications/efficientnet/
- VGG16: https://keras.io/api/applications/vgg/


## Copyright

© 2024 Sarah Temitope Ojo. All rights reserved.

The original source code, model implementations, experimental workflows, analysis, visualisations and documentation in this repository were developed as part of my individual MSc project at the University of Hull.

These original materials may not be reproduced, redistributed, modified or commercially exploited without my prior written permission.

Third-party datasets, libraries, frameworks and pre-trained models remain subject to their respective owners' intellectual property rights and licensing conditions.
