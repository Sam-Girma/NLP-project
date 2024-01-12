# Afaan Oromo Hate Speech Detection (NLP Project) 🚫🗣️

## Introduction 📝
This project aims to detect hate speech in Afaan Oromo language using Natural Language Processing (NLP) techniques. The code includes a Django web application with a hate speech detection model implemented in Keras. The hate speech detection model is trained on the "Afaan Oromo Hate Speech Dataset" available in the provided CSV file.

## Getting Started 🚀
1. Install the required Python packages using `pip install -r requirements.txt`.
2. Ensure the necessary NLTK resources are downloaded by running `nltk.download('punkt')`.
3. Load the hate speech detection model from the provided path using Keras' `load_model` function:
    ```python
    loaded_model = load_model('C:/Users/Admin/Desktop/mlp/NLP-project/socials/base/model.h5', custom_objects={'recall': recall, 'precision': precision, 'f1': f1})

## Text Preprocessing ✨

The `socials/base/utils.py` file contains functions for text preprocessing, including:

- HTML tag removal ✂️
- Symbol and noise removal 🚮
- Stopword removal 🛑
- Non-alphanumeric word removal ❌

## Hate Speech Detection 🚫🗣️

The hate speech detection model predicts whether a given post contains hate speech. The `Post` model in `socials/base/models.py` includes a method `predict_is_hate` that uses the loaded model to make predictions.

## Usage 💡

1. Integrate the provided code into your Django project.
2. Ensure the hate speech detection model is loaded during application startup.
3. Utilize the `predict_is_hate` method in your views to predict hate speech for each post.
