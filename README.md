# Terrain Recognition Using CNN

## Project Overview
This project focuses on building a deep learning-based terrain recognition system using a Convolutional Neural Network (CNN). The model is designed to classify images into one of four terrain types: **Grassy**, **Marshy**, **Rocky**, or **Sandy**. The primary motivation is to develop a compact and efficient model suitable for deployment on drones or other small-scale systems to aid in autonomous terrain identification. This project was inspired by a problem statement from the **Smart India Hackathon**.

## Dataset Structure
The dataset is organized as follows:
- **data.zip**: A compressed file containing the dataset.
  - **Data Main**: Parent folder after extraction.
    - **train**: Contains subfolders for each terrain category for training data.
    - **val**: Contains subfolders for each terrain category for validation data.
    - **test**: Contains subfolders for each terrain category for testing data.

Each subfolder (e.g., `Grassy`, `Marshy`, `Rocky`, `Sandy`) contains relevant images for that category.

## Project Objectives
- Develop an efficient CNN model to classify terrain types.
- Provide real-time terrain identification capability for drones or other autonomous systems.
- Evaluate model performance using industry-standard metrics and visualizations.

## Prerequisites
- Python 3.7+
- TensorFlow/Keras
- NumPy
- Matplotlib
- scikit-learn

## Installation and Setup
1. **Clone the Repository:**
   ```bash
   git clone <repository_link>
   cd terrain-recognition
   ```

2. **Upload the Dataset:**
   - First upload the `data.zip` file in the gdrive of same g account of colab. ( adjust paths in code)

3. **Run the Code:**
   - Execute the `terrain_recognition.ipynb` notebook.

## Workflow
### 1. Data Preprocessing
- The dataset is automatically extracted from `data.zip`.
- Images are normalized using rescaling (values between 0 and 1).
- Data augmentation techniques, such as horizontal flipping and random zooming, are applied to enhance model generalization.

### 2. Model Architecture
The CNN model comprises:
- **Convolutional Layers:** Extract spatial features from the images.
- **MaxPooling Layers:** Downsample feature maps to reduce computational complexity.
- **Dense Layers:** Fully connected layers for classification.
- **Dropout:** Regularization technique to prevent overfitting.

### 3. Training and Validation
- The model is trained using the **Adam optimizer** and **categorical crossentropy** loss.
- Early stopping is implemented to halt training when validation performance ceases to improve.

### 4. Evaluation
- The model is tested on unseen data to measure accuracy.
- A **classification report** and **confusion matrix** are generated to analyze performance.

## Results
- **Accuracy:** The model achieves high accuracy on the test dataset, demonstrating its effectiveness in terrain classification.
- **Performance Visualizations:**
  - Training and validation accuracy/loss curves.
  - Confusion matrix to visualize class-wise performance.

## Usage
- **Deployable Model:** This lightweight model can be integrated into drone systems for real-time terrain recognition.
- **Extensibility:** The architecture can be further enhanced by adding more classes or incorporating advanced features like transfer learning.

## Example Output
### Classification Report
```
              precision    recall  f1-score   support
    Grassy       0.95       0.96      0.95       100
    Marshy       0.93       0.92      0.92       100
    Rocky        0.94       0.91      0.92       100
    Sandy        0.92       0.95      0.93       100

   accuracy                           0.93       400
  macro avg       0.93       0.93      0.93       400
weighted avg       0.93       0.93      0.93       400
```

### Confusion Matrix
![Confusion Matrix](confusion_matrix.png)

## Future Improvements
- Implement transfer learning using pre-trained models like VGG16 or ResNet.
- Optimize the model for better performance on low-resource devices.
- Expand dataset with diverse terrains and environmental conditions.

## Credits
This project was developed as part of the **Smart India Hackathon** problem statement for autonomous systems.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

