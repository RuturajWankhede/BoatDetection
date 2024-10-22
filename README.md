# Boat Detection with CNN and MobileNet

This project focuses on detecting and classifying different types of boats using deep learning models. It utilizes a Convolutional Neural Network (CNN) and a mobile-deployable version of MobileNet for classification, trained on images from 9 different boat categories.

## Table of Contents
1. [Project Structure](#project-structure)
   - [1. Dataset Preparation](#1-dataset-preparation)
   - [2. Model Architecture](#2-model-architecture)
   - [3. Model Training](#3-model-training)
   - [4. Evaluation](#4-evaluation)
   - [5. Performance Comparison](#5-performance-comparison)
2. [Key Insights](#key-insights)
3. [Suggestions for Improvement](#suggestions-for-improvement)
4. [Conclusion](#conclusion)
5. [Future Work](#future-work)

## Project Structure

### 1. Dataset Preparation
The project starts by loading images from a dataset containing 9 classes of boats. A validation split is used to create training and validation sets from the 1162 available images.

- **Screenshot**: A sample of image loading with class labels.

### 2. Model Architecture
Two models were used:
- A **Convolutional Neural Network (CNN)** was built for initial classification.
- A **MobileNetV2**-based lighter model was also trained to be more suitable for mobile deployment.

- **Screenshot**: Model summary showing the architecture of the CNN.

![CNNSUmmary](https://github.com/user-attachments/assets/392f4160-1f2c-40d8-9bea-d51435ce7063)

- **Screenshot**: Model summary showing the architecture of MobileNetV2.

### 3. Model Training
Both models were trained on the dataset with categorical cross-entropy as the loss function and metrics like accuracy, precision, and recall.

- **Screenshot**: Training and validation accuracy plot over 20 epochs for the CNN model.

![CNNTraining](https://github.com/user-attachments/assets/dc978740-b017-4fd4-b45a-93e5d30a4f17)

- **Screenshot**: Training and validation accuracy plot over 50 epochs for the MobileNet model.

![mobilenetTraining](https://github.com/user-attachments/assets/6fb05580-f578-45f8-ac4c-3ea9110775a6)


### 4. Evaluation
Both models were evaluated on the test set, and confusion matrices were plotted to visualize classification performance.

- **Screenshot**: Confusion matrix heatmap for the CNN model.

![confusionmatrixCNN](https://github.com/user-attachments/assets/9e00ed31-c576-48b9-a9bc-3eff5a3249ac)

- **Screenshot**: Confusion matrix heatmap for the MobileNet model.

### 5. Performance Comparison
- The CNN model showed better precision but lower recall, while MobileNet had better recall but lower precision. Both models had accuracy around 36%.
  
- **Screenshot**: Comparison of precision, recall, and accuracy between the CNN and MobileNet models.

## Key Insights
- The CNN model is more confident in its predictions but tends to miss many correct classifications (lower recall).
- The MobileNet model generalizes better to unseen data with a higher recall but tends to make more incorrect predictions (lower precision).

## Suggestions for Improvement
1. **Improve Recall for the CNN Model**: By tuning hyperparameters or introducing regularization techniques, the model’s recall could be improved.
2. **Further Fine-tuning of MobileNet**: Adding more layers or experimenting with different loss functions could help to improve precision and accuracy.
3. **Data Augmentation**: Apply techniques like rotation, flipping, or zooming to augment the dataset and improve model generalization.

## Conclusion
The project demonstrated the use of both deep learning and lightweight models for boat detection. While the results are promising, there’s significant room for improvement in terms of both accuracy and precision.

## Future Work
- Fine-tune both models by adjusting hyperparameters to improve performance.
- Explore more complex architectures or use transfer learning from pre-trained models like EfficientNet.

