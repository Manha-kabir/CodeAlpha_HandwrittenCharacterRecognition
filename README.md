# Handwritten Digit Recognition (CNN on MNIST)

CodeAlpha Internship – Machine Learning project.

A convolutional neural network built with TensorFlow/Keras that recognises handwritten digits (0–9) from the MNIST dataset.

## Results
- Trained on **54,000** images (60,000 MNIST train images, 10% held out for validation)
- **5 epochs**, batch size 64, Adam optimiser
- **98.97% accuracy** on the 10,000-image MNIST test set
- Classification report and confusion matrix in the notebook

## Model
```
Conv2D(32, 3x3, ReLU) -> MaxPool(2x2)
Conv2D(64, 3x3, ReLU) -> MaxPool(2x2)
Flatten -> Dense(128, ReLU) -> Dense(10, softmax)
```
~225K trainable parameters. Loss: sparse categorical cross-entropy.

## Pipeline
1. Load MNIST via `keras.datasets.mnist`
2. Normalise pixels 0–255 to 0.0–1.0 and add a channel dimension (28x28x1)
3. Split off a validation set with `train_test_split`
4. Train the CNN, plot loss/accuracy curves
5. Evaluate on the test set, print classification report and confusion matrix
6. Save the trained model to `models/mnist_cnn.h5`

## Run it
```bash
pip install -r requirements.txt
jupyter notebook notebooks/hand_written.ipynb
```

## Structure
```
models/mnist_cnn.h5          # trained model
notebooks/hand_written.ipynb # full pipeline
requirements.txt
```
