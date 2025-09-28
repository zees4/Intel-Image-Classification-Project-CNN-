# Intel-Image-Classification-Project-CNN-

## Project Overview

This project implements a Convolutional Neural Network (CNN) to classify natural scene images into six categories using the Intel Image Classification Dataset and Google Colab with a GPU T4.

The notebook follows a structured ML pipeline:

- Dataset setup and splitting

- Data preprocessing and augmentation

- CNN model architecture design

- Model evaluation on test data

- Converting the results for further deployment

### The main objective is to build a CNN that achieves ≥85% accuracy on training and testing datasets while following the required architecture rules.

### Dataset

Source: Intel Image Classification Dataset (Kaggle)

Original structure contained train/ and test/ folders.

To meet project requirements:

Combine the folders into a single dataset or choose one file if the minimum requirement is met (min. 1000 entries of data).

Re-split into train (70%), validation (15%), and test (15%) using split-folders.

Classes:

- Buildings

- Forest

- Glacier

- Mountain

- Sea

- Street

### Data Preprocessing

- Image resizing → (150, 150, 3)

- Normalization → pixel values rescaled to [0,1]

- Data augmentation (train only):

- Random rotation

- Width/height shift

- Shear

- Zoom

- Horizontal flip

Tools used: ImageDataGenerator from Keras.

### Model Architecture

The CNN was built using Keras Sequential API to fulfill the project requirements (Sequential, Conv2D, and Pooling layers).

Architecture:

- Convolutional Blocks (x4)

- Conv2D → BatchNormalization → MaxPooling2D

- Flatten layer

- Dense(512) + Dropout(0.5)

- Output layer (Dense, softmax)

This deeper CNN ensures the model can capture more complex features and generalize well.

### Model Training

Loss Function: Categorical Crossentropy

Optimizer: Adam

Metrics: Accuracy


The model was trained for up to 50 epochs, with early stopping to avoid overfitting.

### Evaluation & Results

Training accuracy: >85%

Validation accuracy: >85%

Test accuracy: 85–90%

The test set was only used once at the end to confirm final model performance.
