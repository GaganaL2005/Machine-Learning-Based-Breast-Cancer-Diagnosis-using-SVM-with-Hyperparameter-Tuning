````markdown
# 🎗️ Breast Cancer Prediction Web Application (SVM + Flask)

## 📌 Project Overview

This project is a **Machine Learning-based Breast Cancer Prediction System** built using:

- Flask (Web Framework)  
- Support Vector Machine (SVM)  
- Scikit-learn  
- NumPy  

The application predicts whether a tumor is **High Risk (Malignant)** or **Low Risk (Benign)** based on medical input features.

This is a **Binary Classification Project**.

---

## 🎯 Objective

The main objectives of this project are:

- Train an optimized SVM classifier  
- Perform hyperparameter tuning using GridSearchCV  
- Use cross-validation for reliable evaluation  
- Deploy the trained model using Flask  
- Provide probability-based prediction results  

---

## 📂 Dataset Used

The project uses the **Breast Cancer Wisconsin Dataset** available in Scikit-learn.

### Dataset Information:

- Total Samples: 569  
- Total Features: 30  
- Target Classes:  
  - 0 → Malignant (High Risk)  
  - 1 → Benign (Low Risk)  

The dataset contains various medical measurements computed from digitized images of breast mass cells.

---

## 🧠 Machine Learning Workflow

### 1️⃣ Train-Test Split

The dataset is divided into:

- 80% Training Data  
- 20% Testing Data  

This ensures proper evaluation of the model on unseen data.

---

### 2️⃣ Feature Scaling

Since SVM is sensitive to feature magnitude, **StandardScaler** is applied:

- Mean = 0  
- Standard Deviation = 1  

This improves model performance and stability.

---

### 3️⃣ Model Used – Support Vector Machine (SVM)

The model used:

- `SVC(probability=True)`

SVM is powerful for medical classification tasks and works well with high-dimensional data.

---

### 4️⃣ Hyperparameter Tuning (GridSearchCV)

To find the best model parameters, GridSearchCV is used with:

- C: [0.1, 1, 10]  
- gamma: ['scale', 0.001, 0.01, 0.1]  
- kernel: ['linear', 'rbf', 'poly']  

This automatically selects the best parameter combination using cross-validation.

---

### 5️⃣ Cross-Validation

StratifiedKFold (5 splits) is used to:

- Maintain balanced class distribution  
- Improve model reliability  
- Prevent overfitting  

---

## 📊 Model Evaluation Metrics

The trained model is evaluated using:

### ✅ Accuracy Score  
Measures overall prediction correctness.

### ✅ Classification Report  
Includes:
- Precision  
- Recall  
- F1-Score  

### ✅ Confusion Matrix  
Shows:
- True Positives  
- True Negatives  
- False Positives  
- False Negatives  

These metrics help understand model performance in detail.

---

## 🌐 Flask Web Application

The project includes a user-friendly web interface.

### 🏠 Home Route (`/`)

- Displays input form  
- User enters 5 important medical features:
  - Mean Radius  
  - Mean Texture  
  - Mean Perimeter  
  - Mean Area  
  - Mean Smoothness  

---

### 🔍 Predict Route (`/predict`)

Steps performed:

1. Collect user input  
2. Create full 30-feature array  
3. Fill remaining features with zeros  
4. Scale input using trained scaler  
5. Predict class using best SVM model  
6. Calculate probability score  
7. Display result  

---

## 🧾 Prediction Output

The system displays:

- ⚠️ High Risk of Breast Cancer (Malignant)  
- ✅ Low Risk of Breast Cancer (Benign)  
- Confidence Percentage  

Example Output:

Result: ✅ Low Risk of Breast Cancer  
Confidence: 97.45%

---

## ⚙️ Technologies Used

- Python  
- Flask  
- Scikit-learn  
- NumPy  
- HTML (Frontend Templates)  

---

## 🚀 How to Run the Project

1. Install required libraries:

```bash
pip install flask scikit-learn numpy
```

2. Run the application:

```bash
python app.py
```

3. Open in browser:

```
http://127.0.0.1:5000/
```

---

## 💡 Key Learning Outcomes

- Understanding SVM for classification  
- Importance of feature scaling  
- Hyperparameter tuning using GridSearchCV  
- Cross-validation techniques  
- Deploying ML models using Flask  
- Probability-based medical prediction system  

---

## 📌 Conclusion

This project demonstrates how Machine Learning can be applied in healthcare for early breast cancer risk prediction.

By combining:

- Support Vector Machine  
- Hyperparameter tuning  
- Cross-validation  
- Flask deployment  

We build a complete end-to-end Machine Learning web application.

---

## ⚠️ Disclaimer

This project is developed for educational purposes only.  
It should not be used for real medical diagnosis.  
Always consult a qualified medical professional for actual health concerns.
````
