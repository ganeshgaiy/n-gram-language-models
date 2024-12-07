# Advanced NLP Assignment 1: Language Modeling and Classification

## Introduction
This project explores two foundational NLP tasks:

1. **N-Gram Language Model:** Building an N-gram-based statistical language model for text generation, probability calculation, and perplexity evaluation.
2. **Naive Bayes Classifier:** Implementing a Naive Bayes classifier for text categorization, with applications such as clickbait detection.

## Objectives
- **N-Gram Language Model:**
  - Develop a statistical model to calculate probabilities of word sequences.
  - Evaluate perplexity to measure the model's predictive quality.
  - Generate coherent text sequences.

- **Naive Bayes Classifier:**
  - Train a probabilistic model for text classification tasks.
  - Analyze model performance using accuracy, macro F1-score, and micro F1-score.

## Functionalities
### N-Gram Language Model
- **N-Gram Count:** Tracks unigrams, bigrams, and higher-order N-grams.
- **Smoothing:** Implements Add-K smoothing and linear interpolation for better probability estimates.
- **Perplexity Calculation:** Evaluates the model's ability to predict a given text.
- **Text Generation:** Produces coherent text based on initial prompts.
- **Parameter Optimization:**
  - Finds the optimal smoothing constant (k).
  - Tunes interpolation weights (\( \lambda \)).

### Naive Bayes Classifier
- **Training:** Learns text features and computes category probabilities based on N-grams.
- **Classification:** Categorizes text inputs into predefined classes (e.g., legitimate vs. clickbait headlines).
- **Evaluation:** Measures performance using accuracy, macro F1-score, and micro F1-score.

---

## Workflow
### Language Model (`NGramLM`)
1. **Data Preprocessing:** Tokenizes text and splits it into N-grams.
2. **Model Training:**
   - Stores N-gram counts.
   - Implements smoothing techniques.
3. **Evaluation:** Uses perplexity to assess predictive quality.
4. **Text Generation:** Generates text sequences based on trained probabilities.

### Naive Bayes Classifier
1. **Data Loading:** Reads datasets for clickbait and legitimate headlines.
2. **Training:** Computes feature probabilities for each class.
3. **Prediction:** Categorizes unseen headlines.
4. **Evaluation:** Measures accuracy and F1-scores for predictions.

## Key Files
- `language_model.py`:
  - Implements the N-Gram Language Model.
  - Key methods:
    - `get_ngram_counts`: Extracts N-gram counts from text.
    - `add_k_smooth_prob`: Computes probabilities with Add-K smoothing.
    - `get_perplexity`: Evaluates the predictive quality of text.
    - `generate_text`: Produces text sequences based on a prompt.

- `naive_bayes.py`:
  - Implements the Naive Bayes Classifier.
  - Key methods:
    - `fit`: Trains the classifier by computing category probabilities.
    - `predict`: Classifies input text into categories.
    - `evaluate`: Computes evaluation metrics.

---


