# **MNIST Digit Classification: An SVM Approach**


## Project Overview
This project implements a Support Vector Machine (SVM) to classify handwritten digits (0-9) using the MNIST dataset. By utilizing an RBF kernel and specialized preprocessing like feature scaling, the project demonstrates how to handle high-dimensional image data for precise multi-class classification.

## Dataset Description
The model uses a subset of the MNIST 784 dataset, which consists of:
. Images: 10,000 samples of 28x28 pixel grayscale images of handwritten digits.
. Features: 784 pixels per image, normalized to a [0, 1] range for optimal SVM performance.
. Target Labels: Integers ranging from 0 to 9 representing the actual digit


## Implementation Steps

. **Data Acquisition**: Fetched the MNIST dataset using fetch_openml and selected a 10,000-sample subset for efficiency.
. **Preprocessing**: Scaled pixel values by dividing by 255.0 to ensure all features fall within the same range, which is critical for SVM convergence.
. **Data Splitting**: Divided the processed data into 80% training and 20% testing sets using train_test_split.
. **Model Selection**: Built an SVM classifier using the Radial Basis Function (RBF) kernel, setting hyperparameters to C=10 and gamma='scale' for non-linear decision boundaries.
. **Hyperparameter Tuning**: Conducted a GridSearchCV to evaluate different kernels (linear, poly, rbf) and gamma values to find the most accurate configuration.


## Model Results
The model achieved high accuracy in distinguishing complex handwritten patterns:
. **Optimized Performance**: The GridSearchCV identified the best configuration for the specific data subset.
. **Evaluation Metrics**: Performance was validated through a comprehensive Confusion Matrix and Classification Report, including Precision, Recall, and F1-score for each digit (0-9).
. **Efficiency**: Recorded total execution times for various kernel configurations, such as RBF at ~2.1s and Polynomial at ~3.9s


## Installation & Usage
. Clone this repository to your local machine.
. Ensure you have the following Python libraries installed:
. Bash
  pip install matplotlib scikit-learn numpy
. Run the Jupyter Notebook or Python script to view the classification results and the confusion matrix visualization.
