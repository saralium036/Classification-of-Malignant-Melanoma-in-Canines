# Classification of Malignant Melanoma in Canines Using Deep Learning

## Project Overview

Malignant melanoma is an aggressive form of cancer that can affect dogs. Accurate identification and classification of melanoma from histopathology images can support veterinary diagnosis and treatment decisions.

This project explores the application of deep learning and computer vision to the classification of canine malignant melanoma using digitised histopathology images.

Using the CATCH (Canine Cutaneous Cancer Histology) dataset, the study investigates how convolutional neural networks and transfer learning models can distinguish melanoma tissue from other tissue types.

Three deep learning architectures were developed and evaluated: a Deep Convolutional Neural Network (DCNN), VGG16 and EfficientNet-B0.

The project demonstrates the potential of artificial intelligence in veterinary histopathology and contributes to research into automated cancer image classification.

## Project Objectives

The main objectives were to:

- Apply deep learning techniques to the classification of canine histopathology images.
- Investigate the use of convolutional neural networks for identifying malignant melanoma.
- Compare the performance of different deep learning architectures.
- Explore transfer learning using established image classification models.
- Evaluate model performance and identify an effective approach for histopathological image classification.

## Dataset

The project uses the **CATCH (Canine Cutaneous Cancer Histology) dataset**, which contains digitised histopathology images of canine cutaneous tumours.

The dataset includes five tissue classes:

| Class | Description |
|---|---|
| Subcutis | Subcutaneous tissue |
| Dermis | Dermal tissue |
| Epidermis | Outer layer of the skin |
| Melanoma | Malignant melanoma tissue |
| Necrosis | Areas of tissue necrosis |

The images are H&E-stained whole-slide histopathology images, providing microscopic tissue information for model development and evaluation.

## Tools and Technologies

- **Python** – Model development and data processing.
- **Deep Learning** – Development and training of neural network models.
- **Convolutional Neural Networks (CNNs)** – Histopathology image classification.
- **VGG16** – Transfer learning architecture.
- **EfficientNet-B0** – Deep learning architecture for image classification.
- **Image Processing** – Preparation of histopathology images for model training and evaluation.

## Methodology

### 1. Data Preparation and Preprocessing

The histopathology images were prepared for deep learning classification.

The preprocessing workflow involved extracting image tiles from whole-slide images and preparing them for model training.

Image preprocessing was necessary to ensure that the input data was suitable for the selected neural network architectures.

### 2. Deep Convolutional Neural Network (DCNN)

A custom Deep Convolutional Neural Network was developed to learn relevant visual features from the histopathology images.

The model was trained to recognise tissue patterns and distinguish between the different tissue classes, including malignant melanoma.

### 3. VGG16

VGG16 was explored as a transfer learning approach.

The pretrained architecture was adapted for the classification task, allowing the model to use previously learned image features while learning patterns relevant to canine histopathology.

### 4. EfficientNet-B0

EfficientNet-B0 was also implemented to investigate the performance of an alternative deep learning architecture.

The model was evaluated alongside the custom DCNN and VGG16 to compare their classification performance.

### 5. Model Evaluation

The three models were evaluated using test accuracy to compare their classification performance.

The reported results were:

| Model | Test Accuracy |
|---|---:|
| Deep Convolutional Neural Network (DCNN) | 91% |
| VGG16 | 96% |
| EfficientNet-B0 | 96% |

VGG16 and EfficientNet-B0 achieved the highest reported test accuracy, both outperforming the custom DCNN.

## Results and Discussion

The results demonstrate the potential of deep learning for canine histopathology image classification.

The custom DCNN achieved 91% test accuracy, while both VGG16 and EfficientNet-B0 achieved 96%.

The results suggest that transfer learning architectures can provide strong classification performance when applied to histopathology image analysis.

However, accuracy alone does not provide a complete picture of model performance, particularly where different tissue classes may have different representation in the dataset.

## Conclusion

This project investigated the use of deep learning for the classification of malignant melanoma in canines using histopathology images.

By developing and comparing a custom CNN, VGG16 and EfficientNet-B0, the study explored different approaches to automated tissue classification.

The results highlight the potential of deep learning and transfer learning in veterinary medical image analysis. Further research and validation would be necessary before such models could be considered for clinical diagnostic use.

## Repository Contents

- `notebooks/` – Jupyter Notebook containing the project implementation and analysis.
- `README.md` – Project documentation.

## Author

**Sarah Temitope Ojo**
