# Smart Spoon Project

This repository contains two AI-powered applications:

1. **Sentiment Analysis & User Behavior Prediction**
2. **Food Recognition with Dietary Advice**

## Project 1: Sentiment Analysis & User Behavior Prediction

This project uses **Natural Language Processing (NLP)** and **Machine Learning** to analyze user sentiment and predict their behavior. It's particularly useful for analyzing social media content, customer reviews, and behavior forecasting for targeted marketing or service improvement.

### Features:
- **Sentiment Analysis**: Classifies text data into positive, negative, or neutral sentiments.
- **User Behavior Prediction**: Leverages data-driven models to predict user actions based on historical behavior.
- **Data Preprocessing**: Includes steps for cleaning and preparing text data for machine learning models.


###Running the Project:
Load the dataset and preprocess the text data.

Train a model using machine learning techniques like Logistic Regression or SVM.

Predict sentiment and behavior of new input data.

Project 2: Food Recognition with Dietary Advice
This application leverages deep learning (CNNs) to identify food items from uploaded images and provide personalized dietary recommendations based on the food type.

Features:
Food Image Recognition: Classifies food images into categories such as "Biryani", "Butter Chicken", etc.

Dietary Advice: Provides nutritional advice based on the recognized food item.

Salt Simulation: A "simulate salt" button is available for providing a sensory feedback option for users based on dietary advice.

Technologies Used:
TensorFlow/Keras: For training the food recognition model.

Streamlit: To build a user-friendly interface for food image uploading and prediction.

Pyngrok: For exposing the app via a public URL.

Model Overview:
The model was trained on a dataset of food images and can classify five food types:

Biryani

Butter Chicken

Gulab Jamun

Palak Paneer

Poha

The model uses MobileNetV2 architecture and is optimized for mobile devices.

Installation:
bash
Copy
Edit
pip install -r requirements.txt
Running the Project:
Ensure that the food_classifier.h5 model is saved in your directory.

Run the Streamlit app using the following command:

bash
Copy
Edit
streamlit run app.py
Once the app is running, it will provide a public URL through ngrok where users can upload food images, and the app will return the predicted food label and dietary advice.

Example Code:
python
Copy
Edit
import numpy as np
from PIL import Image
from tensorflow.keras.models import load_model

# Load model
model = load_model("food_classifier.h5")

# Define labels
class_labels = ["biryani", "butter_chicken", "gulab_jamun", "palak_paneer", "poha"]

# Prediction function
def predict(img):
    img = img.resize((150, 150))
    img_array = np.array(img) / 255.0
    img_array = np.expand_dims(img_array, axis=0)
    prediction = model.predict(img_array)
    class_idx = np.argmax(prediction)
    return class_labels[class_idx]
Streamlit App Customization:
The app UI is styled with custom CSS to create a clean and visually appealing interface. The "simulate salt" button is triggered when the app detects the need for salt simulation in the dietary recommendation.

Public URL:
Once the Streamlit app is running, the following command will provide a public URL:

python
Copy
Edit
public_url = ngrok.connect(8501)
print(public_url)
