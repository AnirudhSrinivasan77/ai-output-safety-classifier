# AI Output Safety Classifier

## Project Overview

This project implements a machine learning system designed to detect **Unsafe or Harmful AI-generated Outputs** using Natural Language Processing (NLP) techniques. The model analyzes text inputs and classifies them into **Safe** or **Unsafe** categories.

The system is built using a **BERT-based transformer model** and trained on a combination of multiple publicly available datasets related to toxic speech, misinformation, and harmful language.

The goal of this project is to explore how machine learning models can be used to improve **AI safety and content moderation** by automatically identifying potentially harmful text outputs.

---

# Model Architecture

The classifier is built using a **BERT transformer model** fine-tuned for binary classification.

Pipeline:

Text Input
→ BERT Tokenizer
→ BERT Encoder (bert-base-uncased)
→ Dropout Layer
→ Fully Connected Layer
→ Output: Safe / Unsafe

---

# Datasets Used

The model is trained on a combined dataset created from multiple sources:

1. **Jigsaw Toxic Comment Dataset**
   Used for detecting toxic and offensive language.

2. **LIAR Dataset**
   Contains labeled political statements for misinformation detection.

3. **Hate Speech Dataset**
   Provides labeled examples of hate speech and offensive language.

4. **TruthfulQA Dataset**
   Contains questions used to evaluate truthfulness and factual accuracy.

All datasets are processed and merged into a single dataset used for model training.

---

# Technologies Used

* Python
* Google Colab
* PyTorch
* Hugging Face Transformers
* BERT (bert-base-uncased)
* Pandas
* NumPy
* Scikit-learn

---

# Project Workflow

The project follows these steps:

1. **Dataset Collection**

   * Download datasets from Kaggle and GitHub repositories.

2. **Data Processing**

   * Clean and combine datasets.
   * Convert all samples into a unified format:

     * Text
     * Label (Safe / Unsafe)

3. **Dataset Splitting**

   * 80% Training data
   * 20% Testing data

4. **Tokenization**

   * Use BERT tokenizer to convert text into input tokens.

5. **Model Training**

   * Fine-tune a BERT model using PyTorch.

6. **Evaluation**

   * Evaluate performance using accuracy metrics.

7. **Inference**

   * Predict whether new text inputs are safe or unsafe.

---

# Model Performance

Example training results from the notebook:

Epoch 1
Train Accuracy: 92.8%
Validation Accuracy: 96.8%

Epoch 2
Train Accuracy: 97.2%
Validation Accuracy: 96.4%

Epoch 3
Train Accuracy: 98.8%
Validation Accuracy: 96.3%

---

# Example Prediction

Example usage of the trained model:

Input:
"You are an boy!"

Output:
Safe

The model processes the input text, tokenizes it using BERT, and outputs a classification label.

---

# Repository Structure

AI-Output-Safety-Classifier
│
├── MEGAPROJECT.ipynb       # Main training and inference notebook
├── README.md               # Project documentation

---

# Running the Project

The easiest way to run this project is using **Google Colab**.

Steps:

1. Open the notebook `MEGAPROJECT.ipynb`
2. Upload required dataset credentials if prompted (e.g., Kaggle API key)
3. Run the notebook cells sequentially
4. The notebook will:

   * Download datasets
   * Process data
   * Train the model
   * Perform predictions

---

# Future Improvements

Potential improvements for the project include:

* Training on larger datasets
* Adding multi-class toxicity detection
* Building a web API for real-time inference
* Deploying the model using a web framework

---

