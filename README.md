# Stair Step Detection and Counting
# Project Overview
This project focuses on detecting and counting steps in images of stairs using machine learning techniques. The goal is to develop a model that accurately predicts the number of steps in an image, which can be useful for applications in navigation, accessibility, and robotics.

We implemented four different models and compared their performance using Mean Absolute Error (MAE) as the primary evaluation metric. While Random Forest performed well on the training and test sets, it showed high MAE on the validation set, indicating potential overfitting.

# Dataset
The dataset consists of images of stairs with labeled step counts. Each image undergoes preprocessing before being fed into the model.

# Data Processing Steps:
Image resizing and normalization

Feature extraction (e.g., edge detection, contour analysis)

Splitting into train, test, and validation sets

# Models Used
We tested four different machine learning models:

Random Forest 🌳 (Best performance on training/test but high validation error)

Linear Regression 📈

Support Vector Regression (SVR) 🤖

K-Nearest Neighbors (KNN) 🔍

The performance was evaluated using MAE, which measures how far the predicted step count is from the actual count.

# Results & Evaluation
Train & Test Performance: Random Forest had the lowest MAE.

Validation Performance: Higher MAE, indicating possible overfitting.

Key Findings:

MAE was chosen over accuracy because step counting is a regression problem, not classification.

Small step count errors are tolerable, making MAE a better metric than MSE (which penalizes large errors too harshly).

# How to Run the Project
1️⃣ Install Dependencies
bash
Copier
Modifier
pip install -r requirements.txt
2️⃣ Run the Model
bash
Copier
Modifier
python train_model.py
3️⃣ Test on New Images
bash
Copier
Modifier
python predict.py --image path/to/image.jpg
# Future Improvements
✔ Implement cross-validation to better estimate generalization performance.
✔ Use feature engineering techniques to improve robustness.
✔ Explore ensemble models to reduce overfitting.

# License
This project is open-source and available under the MIT License.

