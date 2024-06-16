# Sentiment Analysis with BERT Variants and Adversarial Training

This repository contains an experiment comparing traditional BERT, whole word masking BERT, and whole word masking BERT with adversarial training for sentiment analysis of car reviews dataset. The goal is to evaluate the performance improvements offered by adversarial training on the sentiment classification task.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Models](#models)
- [Adversarial Training](#adversarial-training)
- [Installation](#installation)
- [Results](#results)
- [Contributing](#contributing)
  
## Introduction

This project implements sentiment analysis using different variants of BERT models. Specifically, it compares the performance of:
- Traditional BERT
- Whole Word Masking BERT
- Whole Word Masking BERT with Adversarial Training

Adversarial training involves generating adversarial examples during training to improve the robustness of the model.

## Dataset

The sentiment dataset used in this experiment consists of reviews labeled as 'positive', 'neutral', or 'negative'. The dataset is loaded from a CSV file and preprocessed to convert sentiments into numerical values.

## Models

The following models are used in the experiment:
- **Traditional BERT**: `bert-large-uncased`
- **Whole Word Masking BERT**: `bert-large-uncased-whole-word-masking`
- **Whole Word Masking BERT with Adversarial Training**: `bert-large-uncased-whole-word-masking` with adversarial example generation

## Adversarial Training

Adversarial training is implemented by generating adversarial examples using the gradient of the loss with respect to the input data. These adversarial examples are then used during the training process to improve model robustness.

## Installation

To run this experiment, you need to install the required libraries. You can do this using the following command:

pip install torch transformers scikit-learn pandas tqdm matplotlib


## Results
The experiment results show that adversarial training did a slight improvement over the traditional and whole word masking BERT models. The traditional BERT model achieved an accuracy of 75.87%, the BERT with Whole Word Masking model improved accuracy to 75.87%, and the BERT with Whole Word Masking and Adversarial Training model reached the highest accuracy of 78.85%.

## Contributing
Contributions to improve this experiment or expand its scope are welcome. You can contribute by:  

-Adding new BERT variants or other transformer models for comparison.  
-Testing different hyperparameters or preprocessing techniques.  
-Implementing additional evaluation metrics or visualization tools.  
