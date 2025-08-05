# Next Word Prediction with LSTM & GRU

This project is a deep learning model designed to predict the next word in a given sequence of text. It uses Recurrent Neural Networks (RNNs), specifically **LSTM (Long Short-Term Memory)** and **GRU (Gated Recurrent Unit)** models, to understand the context and patterns in language.

## What This Project Does

The core idea is to train a model that can learn the structure of a language from a text corpus. Here's the simple breakdown of the process:

1.  **Read Data:** The model is trained on a large text file (e.g., a collection of news articles, a book, etc.).
2.  **Text Cleaning:** The text is cleaned by removing punctuation and converting it to lowercase.
3.  **Tokenization:** The text is broken down into individual words (tokens), and a vocabulary is built. Each unique word is assigned a unique number.
4.  **Create Sequences:** We create input sequences (a series of words) and their corresponding labels (the word that comes next).
    * For example, from the sentence "the cat sat on the mat", we can create the sequence `[the, cat, sat, on, the]` and the label `[mat]`.
5.  **Model Training:** An LSTM or GRU network is trained on these sequences. The model learns the probability of a word appearing after a given sequence of words.
6.  **Prediction:** Once trained, you can provide the model with a "seed" text, and it will predict the most likely word to follow.

## Technology Stack

* **Language:** `Python 3`
* **Deep Learning:** `TensorFlow` / `Keras`
* **Numerical Operations:** `NumPy`

## How to Run It

To get the project running locally, follow these steps.

**1. Clone the repository:**
```bash
git clone [https://github.com/](https://github.com/)[muhammed-rishad-c]/[next-word-prediction].git
cd [your-repo-name]
```

**2. Install dependencies:**
```bash
pip install -r requirements.txt
```
*(Make sure you have a `requirements.txt` file with libraries like `tensorflow` and `numpy` listed).*

**3. Run the prediction script:**
```bash
python predict.py
```

## Usage Example

To predict the next word, you can run the prediction script and provide a starting phrase (seed text).

**Command:**
```bash
python predict.py --seed "the sky is"
```

**Expected Output:**
```
Seed Text: "the sky is..."
Predicted Next Word: blue
```

Or, if your script is interactive:
```
Enter your seed text: the best thing about AI is
> a
> the best thing about AI is its ability...
```
