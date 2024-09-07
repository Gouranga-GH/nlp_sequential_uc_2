
# NLP Sequential Model Project

## Problem Statement
The goal of this project is to build two sequential NLP models for text classification using two distinct datasets:

1. **Sentiment Analysis Model:** This model analyzes customer reviews from the IMDB database to determine whether a review is positive or negative.
2. **Sarcasm Detection Model:** This model detects sarcasm in news headlines using a bidirectional LSTM (Long Short-Term Memory) network.

Both models aim to provide insights by accurately predicting text classifications based on deep learning techniques.

---

## Project Objectives

### Sentiment Analysis Model (IMDB Dataset):
- **Domain:** Digital Content and Entertainment Industry.
- **Objective:** Build a sequential NLP classifier using an IMDB dataset containing 50,000 movie reviews. The task is to classify these reviews as either positive or negative, using sequential models with word embeddings.
- **Data Description:**
  - 50,000 preprocessed movie reviews from IMDB.
  - Each review is encoded as a sequence of word indexes.
  - Vocabulary size: 10,000 (the 10,000 most frequent words).
  - Each word is indexed based on its frequency in the dataset.
  - The integer "0" is used to encode unknown words.
  - Maximum sequence length: 20 words.
- **Key Steps:**
  1. Import and analyze the dataset using the `imdb.load_data()` method.
  2. Perform sequence padding on the dataset to ensure uniform input size.
  3. Build and train a sequential model with embeddings, followed by a classification layer.
  4. Evaluate the model performance on a test set.
  5. Perform predictions on sample reviews.

### Sarcasm Detection Model (News Headlines Dataset):
- **Domain:** Social Media Analytics.
- **Objective:** Detect sarcasm in news headlines using Bidirectional LSTMs. The task is to classify each headline as sarcastic or non-sarcastic based on input text features.
- **Data Description:**
  - Headlines collected from two news websites: TheOnion and HuffingtonPost.
  - Attributes:
    - `is_sarcastic`: 1 if sarcastic, 0 otherwise.
    - `headline`: The actual headline text.
    - `article_link`: A link to the original news article (not used in model training).
- **Key Steps:**
  1. Import and explore the dataset.
  2. Perform text preprocessing and extract relevant columns.
  3. Analyze sentence lengths and prepare word indices.
  4. Create a weight matrix using GloVe embeddings for word representations.
  5. Define and compile a Bidirectional LSTM model.
  6. Train and evaluate the model using validation accuracy.
  7. Test the model on sample headlines to predict sarcasm.

---

## Data Sources
1. **IMDB Movie Reviews Dataset:** A dataset containing 50,000 labeled movie reviews.
2. **News Headlines Dataset for Sarcasm Detection:** Collected from TheOnion and HuffingtonPost news websites.

---

## Key Technologies and Tools
- **Python:** The programming language used for data handling and model building.
- **Keras and TensorFlow:** For building, training, and deploying sequential models.
- **GloVe Embeddings:** Used to represent words in vector form for the sarcasm detection model.
- **Bidirectional LSTM:** A deep learning technique used for capturing the context in sentences for sarcasm detection.

---

## License
This project is licensed under the MIT License.
