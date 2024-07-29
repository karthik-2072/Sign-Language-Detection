# Sign-Language-Detection

This project demonstrates a sign language detection system using landmark detection with Python and Scikit Learn. The system classifies American Sign Language (ASL) symbols through a three-step process involving data preparation, model training, and performance testing.

## Project Overview

The goal of this project is to develop a classifier that can recognize ASL symbols from live webcam data by detecting hand landmarks. The project involves:
1. **Data Preparation**: Collecting and processing images of hand signs to create a dataset.
2. **Model Training**: Using Scikit Learn to train a Random Forest Classifier.
3. **Performance Testing**: Evaluating the model using live webcam data.

## Features

- **Hand Detection**: Detects hand landmarks in real-time using MediaPipe.
- **Landmark Extraction**: Converts hand images into arrays of landmarks for classification.
- **Model Training**: Uses Scikit Learn’s Random Forest Classifier to train the model.
- **Live Testing**: Classifies sign language symbols using live webcam data.

## Installation

To run this project, you need to install the following Python libraries:

- `numpy`
- `opencv-python`
- `mediapipe`
- `scikit-learn`
- `pickle-mixin`





## Usage
### Prepare the Data
Run the Data Collection Script:

Execute the provided Python script to collect images of ASL symbols from your webcam. The script will prompt you to display each symbol in front of the camera.
Images will be saved in directories named after each ASL symbol (e.g., A/, B/, L/).(collect_data.py)
Ensure that the script captures enough images for each symbol to create a robust dataset.

### Train the Model
#### 1. Extract Hand Landmarks:

Use the collected images to extract hand landmarks. Each image's landmarks are converted into an array of coordinates.

#### 2. Create Datasets:

Organize the extracted landmarks and corresponding labels into arrays.
#### 3. Train the Classifier:

Use Scikit Learn to train a Random Forest Classifier with the dataset of landmarks and labels. This step involves splitting the data into training and test sets, training the classifier, and evaluating its performance.(train_model.py)

### Test the Model
#### Classify Symbols from Live Webcam Data:

Run the testing script to use the trained model for classifying ASL symbols in real-time from webcam data. The script will draw bounding boxes and labels on the webcam feed to indicate detected symbols.(python test_model.py)


## Conclusion
This project successfully demonstrates a comprehensive approach to sign language detection using machine learning and computer vision techniques. By leveraging MediaPipe for hand landmark detection and Scikit Learn for training a Random Forest Classifier, the system achieves efficient and accurate classification of ASL symbols. The process of data preparation, model training, and performance testing ensures the robustness and reliability of the classifier. This project provides a strong foundation for further improvements and potential applications in real-time sign language interpretation and other gesture recognition systems.
