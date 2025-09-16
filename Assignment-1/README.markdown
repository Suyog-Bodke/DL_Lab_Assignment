# MNIST Handwritten Digit Classification

## Overview
This project implements a neural network using TensorFlow and Keras to classify handwritten digits from the MNIST dataset. The model is trained to recognize digits from 0 to 9 based on 28x28 pixel grayscale images.

## Requirements
To run this project, you need the following dependencies:
- Python 3.x
- TensorFlow (`tensorflow`)
- Matplotlib (`matplotlib`)

You can install the dependencies using pip:
```bash
pip install tensorflow matplotlib
```

## Dataset
The MNIST dataset is used, which consists of:
- **Training set**: 60,000 images of handwritten digits
- **Test set**: 10,000 images of handwritten digits
Each image is a 28x28 grayscale image, and the labels are integers from 0 to 9.

## Model Architecture
The neural network is built using a Sequential model in Keras with the following layers:
1. **Flatten**: Converts the 28x28 input images into a 1D array (784 units).
2. **Dense (128 units)**: Fully connected layer with ReLU activation.
3. **Dense (64 units)**: Fully connected layer with ReLU activation.
4. **Dense (10 units)**: Output layer with softmax activation for 10-class classification.

## Preprocessing
- The pixel values of the images are normalized to the range [0, 1] by dividing by 255.0.
- The labels are converted to one-hot encoded format using `to_categorical`.

## Training
The model is trained with the following configuration:
- **Optimizer**: Adam
- **Loss Function**: Categorical Crossentropy
- **Metrics**: Accuracy
- **Batch Size**: 32
- **Epochs**: 10
- **Validation Split**: 20% of the training data is used for validation.

## Evaluation
The model is evaluated on the test set to compute the test loss and accuracy. The results are printed after training.

## Usage
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd <project-directory>
   ```
3. Run the Python script (e.g., `main.py`):
   ```bash
   python main.py
   ```
   This will load the MNIST dataset, preprocess the data, train the model, and output the test loss and accuracy.

## Results
After training, the model achieves a test accuracy of approximately [insert typical accuracy, e.g., 97-98%] on the MNIST test set. The exact accuracy may vary slightly depending on the random initialization and training process.

## Files
- `main.py`: The main script containing the code for loading data, building and training the model, and evaluating performance.
- `README.md`: This file, providing an overview and instructions for the project.
