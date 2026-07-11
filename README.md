# Cat vs Dog Classifier

A computer vision project that classifies images as cat or dog, with a confidence score, deployed as an interactive web app.

## Overview

This project uses transfer learning to build an image classifier without training a neural network from scratch. A pre-trained MobileNetV2 (trained on ImageNet) is used as a frozen feature extractor, with a custom classification head trained on top of it to distinguish cats from dogs.

## Tech Stack

- **TensorFlow / Keras** — model building and training
- **MobileNetV2** — pre-trained base model (transfer learning)
- **Hugging Face Datasets** — cats vs dogs dataset (2,500 images)
- **scikit-learn** — train/test split
- **Streamlit** — web app for live predictions
- **Google Colab** — training environment

## How It Works

1. Load and preprocess images (resize to 224×224, normalize)
2. Split into training (80%) and testing (20%) sets
3. Load MobileNetV2 with frozen weights, add a new dense output layer
4. Train the new layer for 5 epochs
5. Evaluate accuracy on the test set
6. Deploy as a Streamlit app — upload an image, get a prediction with confidence %

## Running It Yourself

1. Open `Cat_and_Dog_Classifier.ipynb` in Google Colab
2. Run all cells in order
3. To launch the web app, run the final cells (requires a free [ngrok](https://ngrok.com/) auth token, which you'll need to add yourself)

## Demo

A video demo showing live predictions is linked in the www.linkedin.com/in/aaryan-dabhade-0694903b9 about this project.

## Notes

This was built as a hands-on learning project to understand the full ML workflow — data preparation, transfer learning, evaluation, and deployment — end to end.
