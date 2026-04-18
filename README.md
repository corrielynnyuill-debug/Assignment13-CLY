# Assignment13-CLY
Assignment 13 Generative AI Essentials Project Gutenberg (http://www.gutenberg.org/)

# Overview
This project explores the fundamentals of Generative AI through the implementation of a character‑level LSTM text generation model trained on Alice’s Adventures in Wonderland from Project Gutenberg. The goal is to demonstrate how generative models learn patterns in text and produce new sequences based on a seed prompt.

The work includes:

Dataset preparation and cleaning
Character‑level tokenization
Building and training an LSTM model in TensorFlow/Keras
Implementing temperature‑controlled text generation

A brief application demo using custom seed prompts

This project was developed in Google Colab and submitted as part of a Generative AI coursework assignment.

# Dataset
Source: Project Gutenberg
Text: Alice’s Adventures in Wonderland (public domain)
The text is downloaded programmatically, cleaned by removing Gutenberg headers/footers, and normalized for training.

# Model Architecture
A lightweight generative model was implemented using TensorFlow/Keras:

Embedding layer (64 dimensions)
LSTM layer (128 units)
Dense output layer with softmax activation

The model predicts the next character in a sequence given the previous 40 characters.

# Training
50,000 training sequences
Sequence length: 40 characters
Batch size: 128
Epochs: 30
Loss function: sparse_categorical_crossentropy
Optimizer: adam

Training was performed on Google Colab using GPU acceleration.

# Text Generation
A temperature‑controlled sampling function was implemented to adjust creativity:

Low temperature (0.5): more stable, predictable text
Higher temperature (0.7+): more creative, chaotic text

Example seed:
"The Caterpillar looked at her and"
The model generates ~400 characters of new text based on learned patterns.

# Application Demo
A simple content‑creation demo is included in the notebook:

User provides a seed phrase
Model generates new text
Temperature parameter controls creativity

This demonstrates the core workflow behind generative text systems.

# Ethical Considerations
The project uses public‑domain text to avoid copyright issues.
Discussion of broader ethical considerations (bias, misinformation, responsible use) is included in the accompanying report.

# License
This project uses public‑domain text from Project Gutenberg.
All code is released under the MIT License.
