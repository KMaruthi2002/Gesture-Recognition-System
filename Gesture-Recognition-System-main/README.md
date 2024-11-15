# hand-gestures-recognition-and-segmentation-using-CNN-and-OpenCV

This GitHub repository contains code for a Convolutional Neural Network (CNN) model to detect five different hand gestures from segmented hand photos. The model is trained on a dataset using Keras with TensorFlow backend and includes data preprocessing, model building, training, and evaluation. Additionally, there is a separate file, "Real_life_test," demonstrating real-time hand gesture recognition using OpenCV.

![Hand Gesture Detection and Segmentation](https://github.com/Sousannah/hand-gestures-recognition-and-segmentation-using-CNN-and-OpenCV/blob/main/Screenshot%202024-01-12%20184453.png)

## Project Structure

The repository is organized as follows:

1. **Data Preparation:**
   - The dataset is stored in the "data" directory, with subdirectories for each class representing different hand gestures. You can download the dataset from [this Kaggle link](https://www.kaggle.com/datasets/sarjit07/hand-gesture-recog-dataset/data) and extract it into the "data" directory.

2. **CNN Model:**
   - The initial model architecture is defined using Keras Sequential API in the main file.
   - The first attempt may show signs of overfitting, so a second model is created with dropout and regularization to address this issue.
   - The third model utilizes a pre-trained ResNet50 model for feature extraction, followed by additional layers for classification.

3. **Training and Evaluation:**
   - The models are trained using the training set and evaluated on the validation and test sets.
   - Training history, loss, and accuracy plots are visualized for each model.
   - Confusion matrices and classification reports provide detailed performance metrics.

4. **Real-time Hand Gesture Recognition:**
   - The "OpenCV_test" file demonstrates how to use OpenCV for real-time hand gesture recognition.
   - It captures video frames from the camera, preprocesses them, and utilizes the trained model to predict gestures.

5. **Dataset Testing:**
   - The "CNN02_Model_Test" file allows testing the trained model on any provided segmented hand photos.
   - Provide the directory path containing the segmented hand photos, and the model will predict the gestures.

## Instructions:

1. **Dataset:**
   - Download the dataset from [Kaggle](https://www.kaggle.com/datasets/sarjit07/hand-gesture-recog-dataset/data) and extract it into the "data" directory.

2. **Training:**
   - Run the "CNN_Train" file to train and evaluate the CNN models.
   - Run the "segmentation_ResNet(one real data)" file to Train and evaluate the ResNet model on the data without doing data augmentation
   - Run the "segmentation_ResNet(one augmented data)" file to Train and evaluate the ResNet model on the data after doing data augmentation
   - Experiment with model architectures and hyperparameters to achieve optimal performance.

3. **Real-time Testing:**
   - Execute the "OpenCV_test" file to see real-time hand gesture recognition using OpenCV.

4. **Model Saving:**
   - The trained models are saved in the repository for later use.

## Requirements:

- Python 3.x
- Libraries: TensorFlow, Keras, OpenCV, scikit-learn, matplotlib, seaborn
**Note: The trained ResNet models perform better than the CNN model**
