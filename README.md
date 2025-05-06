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


## Project 2: Food Recognition with Dietary Advice

This project uses **Deep Learning (CNNs)** to recognize food items from images and provide **personalized dietary recommendations** based on the recognized food. The app is designed to help users make healthier food choices by analyzing food images.

### Features:
- **Food Image Recognition**: Classifies food images into 5 predefined categories: Biryani, Butter Chicken, Gulab Jamun, Palak Paneer, and Poha.
- **Dietary Advice**: Provides specific dietary advice related to each food item, such as recommendations on sodium intake and salt usage.
- **User-Friendly Interface**: Built with **Streamlit** for easy food image uploads and predictions.
- **Model**: Uses a **MobileNetV2** pre-trained model fine-tuned on a custom food image dataset.

### Technologies Used:
- **TensorFlow / Keras**: For training the food recognition model.
- **Streamlit**: To create an interactive front-end for uploading images and viewing predictions.
- **ngrok**: To expose the Streamlit app over the internet.
- **Python**: Primary language for data processing, model training, and app development.

### Running the Project:
1. Ensure that the **food_classifier.h5** model file is available in the project directory.
2.  Start the Streamlit app by running:
    ```bash
    !streamlit run app.py &>/content/logs.txt & 
    ```
3. After running the above command, **Streamlit** will start the app locally.
4. **ngrok** is used to expose the Streamlit app to the internet, allowing you to access it from anywhere:
    - **ngrok** should automatically open a tunnel, but if not, you can manually start it with:
      ```python
      from pyngrok import ngrok
      public_url = ngrok.connect(8501)
      print(f"App is accessible at: {public_url}")
      ```
    - **ngrok** will generate a public URL that you can use to access your app. This URL can be shared with anyone to view the app remotely.

### Sample Usage:
1. **Upload a food image** through the interface.
2. The app will predict the food type and provide **personalized dietary advice**.

### Example Images for Food Prediction with Dietary Advice
![image](https://github.com/user-attachments/assets/bbb87840-ea29-4671-bea8-ebf9a31c0fe8)
![example image](https://github.com/user-attachments/assets/002023b4-4d0b-44f9-843d-6ebf793505d4)
![image](https://github.com/user-attachments/assets/598a03e6-83d3-4b88-98ef-2eb0acdd6b86)
![image](https://github.com/user-attachments/assets/5f9b077b-32b4-46fc-8faf-53aaf8327e09)

### Sentimental Analysis results:
![image](https://github.com/user-attachments/assets/bd240a2b-c23a-473a-83b1-194239ddafbf)
![image](https://github.com/user-attachments/assets/dd42d612-5e67-4612-a32a-fd920df4ac4a)
![image](https://github.com/user-attachments/assets/5e3db676-45ed-4cba-86dc-e750191d03db)




