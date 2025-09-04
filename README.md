# Edunet_Internship-AIML-
Substainable Agriculture

🌱 LeafLens – AI-Powered Eco-Friendly Crop Disease Detection






LeafLens is an AI-driven solution that detects crop diseases from leaf images and provides eco-friendly management advice. It enables farmers, agronomists, and agricultural enthusiasts to monitor crop health efficiently while promoting sustainable practices.

🔹 Features

Accurate Disease Detection: Detects 38 crop disease classes with high precision using a fine-tuned CNN model.

Eco-Friendly Advice: Provides actionable recommendations without harming the environment.

Batch & Single Image Prediction: Supports both bulk uploads and individual image analysis.

Visual Insights: Displays disease predictions with images and Grad-CAM-like visualizations for explainability.

Lightweight Deployment: Model exported to TFLite, ready for mobile and edge devices.

Exportable Reports: Saves predictions and advice into CSV files for record-keeping.

🔹 Supported Crops & Diseases

Apple: Apple Scab, Black Rot, Healthy

Tomato: Late Blight, Early Blight, Healthy

(Full list of 38 classes included in the model)

🔹 Demo Screenshots


Visual prediction with confidence and eco-friendly advice.

🔹 Installation

Clone the repository:

git clone https://github.com/YourUsername/LeafLens.git
cd LeafLens


Install dependencies:

pip install -r requirements.txt


Mount Google Drive if using Colab for dataset/models:

from google.colab import drive
drive.mount('/content/drive')

🔹 Usage
Single Image Prediction
from predict import predict_and_visualize

img_path = 'path_to_leaf_image.jpg'
pred_class, confidence, advice = predict_and_visualize(img_path)

Batch Prediction
from predict import predict_batch_images

batch_results = predict_batch_images(folder_path='batch_images/')

Export TFLite Model
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

Create a feature branch

Submit a pull request

🔹 License

This project is licensed under MIT License. See LICENSE
 for details.

🔹 Tagline

LeafLens – See your crops, save your crops. AI-powered insights, eco-friendly action.
