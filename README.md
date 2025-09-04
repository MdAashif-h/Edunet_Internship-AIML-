# Edunet_Internship-AIML-
Substainable Agriculture

# 🌱 LeafLens – AI-Powered Eco-Friendly Crop Disease Detection

[![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python)](https://www.python.org/)  
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)](https://www.tensorflow.org/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  

---

## Sustainable Agriculture

**LeafLens** is an AI-driven solution that detects crop diseases from leaf images and provides **eco-friendly management advice**. It enables farmers, agronomists, and agricultural enthusiasts to monitor crop health efficiently while promoting sustainable practices.

> **Tagline:** LeafLens – See your crops, save your crops. AI-powered insights, eco-friendly action.

---

## 🔹 Features

- **Accurate Disease Detection** – Detects 38 crop disease classes with high precision using a fine-tuned CNN model.  
- **Eco-Friendly Advice** – Provides actionable recommendations without harming the environment.  
- **Batch & Single Image Prediction** – Supports both bulk uploads and individual image analysis.  
- **Visual Insights** – Displays disease predictions with images and Grad-CAM-like visualizations for explainability.  
- **Lightweight Deployment** – Model exported to **TFLite**, ready for mobile and edge devices.  
- **Exportable Reports** – Saves predictions and advice into CSV files for record-keeping.  

---

## 🔹 Supported Crops & Diseases

- **Apple**: Apple Scab, Black Rot, Healthy  
- **Tomato**: Late Blight, Early Blight, Healthy  
- *(Full list of 38 classes included in the model)*  

---

## 🔹 Eco-Friendly Advice Examples

| Disease Class | Advice |
|---------------|--------|
| Apple___Apple_scab | Remove infected leaves. Apply sulfur-based fungicide. |
| Apple___Black_rot | Prune affected areas and maintain proper sanitation. |
| Apple___healthy | No action needed. Monitor regularly. |
| Tomato___Late_blight | Use copper-based sprays. Avoid overhead watering. |
| Tomato___Early_blight | Rotate crops and remove infected debris. |

---

## 🔹 Demo Screenshot

![LeafLens Demo](demo_screenshot.png)  
*Visual prediction with confidence and eco-friendly advice.*

---

## 🔹 Installation

1. Clone the repository:  
git clone https://github.com/YourUsername/LeafLens.git
cd LeafLens


2. Install dependencies:  
pip install -r requirements.txt

csharp

3. Mount Google Drive if using Colab for dataset/models:  
```python
from google.colab import drive
drive.mount('/content/drive')

🔹 Usage
Single Image Prediction

python

from predict import predict_and_visualize

img_path = 'path_to_leaf_image.jpg'
pred_class, confidence, advice = predict_and_visualize(img_path)
Batch Prediction

python

from predict import predict_batch_images

batch_results = predict_batch_images(folder_path='batch_images/')
Export TFLite Model

python

from export_model import export_tflite_model

export_tflite_model(model_path='models/fine_tuned_model.h5')
🔹 Project Structure

LeafLens/
│
├─ models/
│   ├─ fine_tuned_model.keras
│   ├─ fine_tuned_model.tflite
│   └─ class_indices.npy
│
├─ predict.py          # Functions for prediction & visualization
├─ export_model.py     # Convert Keras model to TFLite
├─ requirements.txt
├─ README.md
└─ demo_screenshot.png
🔹 Technologies Used
Python 3.12

TensorFlow 2.x / Keras – CNN-based fine-tuned model

NumPy & Pandas – Data processing

Matplotlib – Visualizing predictions

Google Colab / Drive – Dataset and model storage

TFLite – Lightweight deployment for mobile/edge

🔹 Contribution
Contributions are welcome!

Fork the repository

Create a feature branch (git checkout -b feature-name)

Commit your changes (git commit -m 'Add feature')

Push to the branch (git push origin feature-name)

Open a Pull Request

🔹 License
This project is licensed under the MIT License – see LICENSE for details.
