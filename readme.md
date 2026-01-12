
# Phishing Website Classification Project

This repository contains the code for a machine learning-based phishing detection project. The project uses a multi-modal approach, analyzing **URL/DNS**, **HTML Structure**, and **Page Content** to classify websites as benign or phishing.

## Project Structure

The project is organized into three main stages: Feature Extraction, Base Model Training, and Meta-Model Stacking.

### 1. Feature Extraction
Notebooks responsible for parsing raw data and generating numerical features.
* **`html_Features_extraction.ipynb`**: Parses raw HTML content to extract the 37 features used for classification.
* **`Features_extraction.ipynb`** : Extracts all the other raw features that are not html.


### 2. Base Model Training
Notebooks for training and evaluating individual classifiers for each domain.
* **`html_classification.ipynb`**: Trains and evaluates models (Random Forest, XGBoost, etc.) specifically on the extracted HTML features.
* **`url_dns_ssl_classification.ipynb`** *(if applicable)*: Training pipeline for the URL-based model.
* **`content_classification.ipynb`** *(if applicable)*: Training pipeline for the Content-based model.

### 3. Stacking & Meta-Learning
The final ensemble model that combines the predictions of the base models.
* **`meta_learner.ipynb`**: Implements the Stacking Ensemble. It loads the pre-trained base models, generates Out-of-Fold (OOF) predictions, and trains the Meta-Learner (Logistic Regression) to make the final prediction.

### 4. Data
* **`dataset/`**.
