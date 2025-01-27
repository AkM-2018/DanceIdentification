## Dance Classification using VGG16
This project focuses on classifying different Indian dance forms using transfer learning with a pre-trained VGG16 model. The dataset includes images from eight dance categories, and the final predictions are output as a CSV file. The project demonstrates skills in Python, TensorFlow, Pandas, and data visualization with Matplotlib.

## Features
**Preprocessing**: Data is prepared for training, validation, and testing using TensorFlow's ImageDataGenerator.
Transfer Learning: Utilized the VGG16 model, modified to classify eight dance categories by adding a custom dense layer.
**Visualization**: Matplotlib is used for data exploration and results visualization.
**Submission**: Predicted dance categories are saved as a CSV file.

## Dataset
The dataset is structured into three directories:

- **train**: For training the model.
- **valid**: For validation during training.
- **test**: For making final predictions.

The images are organized into subfolders for each dance type:
- Bharatanatyam
- Kathak
- Kathakali
- Kuchipudi
- Manipuri
- Mohiniyattam
- Odissi
- Sattriya

## Code Workflow
#### **Data Preparation**
Mounted Google Drive to access the dataset.
Used TensorFlow's ImageDataGenerator for preprocessing (resizing images to 224x224 and normalizing pixel values).
Split images into training and validation sets.
#### **Model Modification**
Loaded the pre-trained VGG16 model.
Removed the top layer and added a dense layer with 8 output neurons (softmax activation) for multi-class classification.
Set pre-trained layers to non-trainable to retain VGG16's learned features.
#### **Training**
Compiled the model with Adam optimizer and categorical_crossentropy loss.
Trained the model for 10 epochs using training and validation datasets.
#### **Predictions**
Made predictions on the test set using the trained model.
Mapped predicted labels to corresponding dance categories.
#### **Submission**
Generated a CSV file containing the image names and their predicted dance categories.


## Key Python Libraries Used
- **TensorFlow/Keras**: For model creation, training, and predictions.
- **NumPy**: For array manipulations.
- **Matplotlib**: For data visualization.
- **Pandas**: For creating the submission file.
