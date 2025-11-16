🧠 Handwritten Character Recognition
CodeAlpha Internship – Machine Learning Project

This project is part of the CodeAlpha Internship Program.
The goal is to build a machine learning model that can read and recognize handwritten characters using deep learning (CNN).

📌 Project Overview

Handwritten Character Recognition means teaching a computer to look at an image of a letter or number and correctly identify what it is.

In this project, I used:

EMNIST dataset → images of handwritten letters

Python

TensorFlow/Keras → to build the Convolutional Neural Network (CNN)

Jupyter Notebook → for running the code step-by-step

🗂 Folder Structure
Handwritten_Character_Recognition/
│
├── data/                       # Dataset files (EMNIST)
├── models/                     # Saved trained models (.h5 files)
├── src/                        # Source code
│   ├── load_data.py
│   ├── train_model.py
│   ├── evaluate_model.py
│   └── predict.py
│
├── notebooks/
│   └── character_recognition.ipynb
│
├── requirements.txt
├── .gitignore
└── README.md

🔧 Technologies Used

Python 3.10+

Jupyter Notebook

TensorFlow / Keras

NumPy

Matplotlib

scikit-learn

To install dependencies:

pip install -r requirements.txt

📥 Dataset

This project uses the EMNIST Letters Dataset, which contains 28×28 pixel grayscale images of handwritten alphabets.

Dataset link (official):
https://www.nist.gov/itl/products-and-services/emnist-dataset

The dataset loads automatically through TensorFlow/Keras during execution.

🧪 How the Project Works
1️⃣ Data Loading

The dataset is loaded, reshaped, and normalized so the model can understand the images.

2️⃣ Data Preprocessing

Pixel values are scaled (0–255 → 0–1)

Labels are converted into numerical categories

Data is split into training and testing

3️⃣ Model Building (CNN)

A Convolutional Neural Network (CNN) is used because it works best for image recognition tasks.

The model contains:

Convolution layers

Max-Pooling layers

Dense layers

Softmax output layer

4️⃣ Training

The model learns patterns in handwritten characters.

5️⃣ Evaluation

Accuracy and loss are calculated using test data.

6️⃣ Saving

The trained model is saved into /models/model.h5

▶️ How to Run the Project
Option A — Run the Notebook

Open terminal

Run:

jupyter notebook


Open the file:

notebooks/hand_written.ipynb


Run all cells.

Option B — Run as Python Script
python src/train_model.py
python src/evaluate_model.py

📊 Results

The final CNN model achieves high accuracy in recognizing handwritten characters from EMNIST.

Accuracy varies depending on the number of training epochs.

Example:

Training Accuracy: ~99%
Testing Accuracy:  98%

🎥 Project Video

A video explanation of the project has been uploaded on LinkedIn as required for the internship.

🔗 GitHub Repository:

https://github.com/Manha-kabir/CodeAlpha_HandwrittenCharacterRecognition