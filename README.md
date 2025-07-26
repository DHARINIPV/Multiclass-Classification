# Multiclass Animal Image Classification using CNN (TensorFlow)

## Problem Statement
The goal of this project is to develop and implement a robust multiclass image classification model capable of accurately identifying and categorizing images of dogs, cats, and pandas. This addresses the challenge of distinguishing between visually similar animal species within a given dataset, aiming to achieve high classification accuracy through the application of deep learning techniques, specifically Convolutional Neural Networks (CNNs). The project seeks to build an automated system that can reliably classify these animal images, which has potential applications in various fields such as wildlife monitoring, content organization, and educational tools.

## Step-by-Step Rundown:

### Step 1: Prepare Kaggle Credentials:

-> Make sure that you have your kaggle.json file (with your Kaggle API credentials).

-> Put this file in the right directory (~/.kaggle/) and execute the proper permissions to protect your API key. 

-> Use the Kaggle API to download the "dogcatpanda" dataset into your environment directly.

-> Unzip the downloaded dataset to make image files available for processing.

### Step 2: Import Libraries

-> Import relevant deep learning, image processing, and data manipulation libraries. These usually consist of tensorflow, keras, numpy, and matplotlib.pyplot.

-> Create ImageDataGenerator for your training, validation, and test sets.

-> Setup parameters for data augmentation (e.g., rescale, rotation, shear, zoom, flip horizontal) on the training data to enhance dataset diversity and support model generalization.

-> Identify target image dimensions, batch size, and class mode (categorical for multiclass classification).

### Step 3: Construct the CNN Model:

-> Specify the architecture of the Convolutional Neural Network.

Conv2D layers for extracting features.

MaxPooling2D layers for down-sampling.

Flatten layer to transform 2D feature maps to a 1D vector.

Dense layers for classification head.

Dropout layers to avoid overfitting.

Make sure the last Dense layer has a softmax activation function with the number of units being your number of classes (i.e., 3 for dog, cat, panda).

### Step 4: Compile the Model:

-> Configure the model for training by defining:

Optimizer: adam is widely used.

Loss Function: categorical_crossentropy for multiclass classification.

Metrics: accuracy to track performance during training.

Set Up Callbacks: Apply EarlyStopping callback to track a metric (e.g., val_loss) and terminate training if it doesn't improve for a certain amount of epochs (patience). It prevents overfitting and conserves computational resources.

### Step 5: Train the Model:

-> Train the model on training data using model.fit().

-> Pass the training data generator, validation data generator, number of epochs, and any callbacks that are set.

### Step 6: Test Model Performance:

After training, test the model on the test dataset to determine its ability to generalize on unseen data.

### Results: 

-> Training Accuracy: 88.84%

-> Validation Accuracy: 73.33%

<img width="751" height="577" alt="image" src="https://github.com/user-attachments/assets/2c8bca3b-b3bd-43e1-8803-411720340843" />

<img width="753" height="578" alt="image" src="https://github.com/user-attachments/assets/b0279cbd-d88d-4136-9539-53efdf0917da" />

#### Prediction: 
<img width="705" height="681" alt="image" src="https://github.com/user-attachments/assets/faca5b1c-b068-4761-8709-b5388f04837c" />

#### Confusion Matrix:
<img width="740" height="608" alt="image" src="https://github.com/user-attachments/assets/149ff530-4f51-431f-9fb4-a8fa7910b2d0" />

##  Final Goal:
To accurately classify animal images into three categories using a CNN. It's a beginner-friendly, real-world application of deep learning in image classification.



