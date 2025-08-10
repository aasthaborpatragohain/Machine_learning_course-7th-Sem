# Assignment 1: Digit Classification with TensorFlow

##  Project Description
This project demonstrates how to build, train, and evaluate a simple Neural Network on the *MNIST* handwritten digits dataset using *TensorFlow/Keras* in Python.  
It follows the complete machine learning workflow — from loading and preprocessing data to training the model, evaluating its accuracy, and making predictions with visualization.  

---

## Dataset
This project uses the *MNIST* dataset, a classic benchmark for handwritten digit recognition:

- *Total images:* 70,000 (28×28 pixels, grayscale)  
- *Training set:* 60,000 images  
- *Test set:* 10,000 images  
- *Labels:* Digits from *0–9*  
- *Source:* Automatically downloaded via tensorflow.keras.datasets — no manual download required.  

---

## Workflow

1. *Import Libraries*  
   - *TensorFlow* → Deep learning framework  
   - *NumPy* → Numerical operations  
   - *Matplotlib* → Visualization of results  

2. *Load the Dataset*  
   - Code:  
     python
     (x_train, y_train), (x_test, y_test) = mnist.load_data()
     

3. *Normalize the Data*  
   - Scale pixel values from *[0, 255]* to *[0, 1]* for better model convergence.  

4. *Build the Model*  
   - *Flatten Layer* → Converts each image to a 1D vector of size 784  
   - *Dense Layer (128, ReLU)* → Learns patterns in data  
   - *Dense Layer (10, Softmax)* → Outputs probabilities for each digit class  

5. *Compile the Model*  
   - *Optimizer:* Adam  
   - *Loss:* Sparse Categorical Crossentropy  
   - *Metric:* Accuracy  

6. *Train the Model*  
   - Trained for *5 epochs* on the training set  

7. *Evaluate the Model*  
   - Test accuracy printed after evaluation  

8. *Make Predictions & Visualize*  
   - Predicts sample images from the test set  
   - Displays images with *green titles* for correct predictions and *red titles* for incorrect ones
