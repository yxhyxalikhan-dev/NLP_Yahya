# Natural Language Processing Lab – Practicals

**Student Name:** Khan Yahya Shahid Ali
**UIN:** 221A048
**Roll No:** 28

This repository contains all the NLP lab experiments, implemented in Python using Jupyter / Google Colab notebooks.

---

## Experiments Overview

| Exp No. | Experiment Name | File Name |
| :---: | :--- | :--- |
| **Exp 2** | Corpus Exploration & Sentiment Analysis using Twitter Samples | `NLP_exp_2.ipynb` |
| **Exp 3a** | Text Preprocessing (Tokenization, Stopword Removal, Stemming & Lemmatization) | `NLP3a.ipynb` |
| **Exp 3b** | Advanced Text Preprocessing (Emoji, URL, Regex Cleaning, Stemming & Lemmatization) | `NLP3b.ipynb` |
| **Exp 4** | Morphological Analysis & Lemmatization | `nlpexp4.ipynb` |
| **Exp 5** | N-gram Language Modeling & Next Word Prediction | `nlpexp5.ipynb` |
| **Exp 5 (Part 2)** | N-gram Language Modeling with Reuters Corpus & Perplexity | `NLPexp5_part_2.ipynb` |
| **Exp 6** | Part-of-Speech (POS) Tagging with Rule-based & N-gram Taggers | `NLP_exp6.ipynb` |
| **Exp 7b** | Named Entity Recognition (NER) using NLTK & spaCy | `NLP7b.ipynb` |
| **Exp 8** | TF-IDF Vectorization & Document Cosine Similarity Analysis | `NLPexp8.ipynb` |
| **Exp 9** | Word Sense Disambiguation (WSD) using Lesk Algorithm | `NLP9.ipynb` |
| **Exp 10** | Exploratory Text Analysis on IMDb Reviews | `Nlp_exp10.ipynb` |

---

## Experiment Details

### Exp 2 – Corpus Exploration & Sentiment Analysis (Twitter Samples)
- Loads the NLTK `twitter_samples` corpus (positive and negative tweets).
- Explores the data and stores the tweets in a pandas DataFrame.
- Visualizes the data using matplotlib.

### Exp 3a – Text Preprocessing
- Tokenization with `word_tokenize`.
- Punctuation and stopword removal.
- Stemming (Porter Stemmer) and Lemmatization (WordNet Lemmatizer).

### Exp 3b – Advanced Text Preprocessing
- Everything in Exp 3a, plus cleaning with regular expressions.
- Handling of emojis (`emoji` library) and URLs.

### Exp 4 – Morphological Analysis & Lemmatization
- Lowercasing, tokenization and punctuation removal.
- Finding root words with the WordNet Lemmatizer (verb / noun / adjective POS).
- Manual analysis of inflectional vs. derivational morphology.

### Exp 5 – N-gram Language Modeling & Next Word Prediction
- Text preprocessing (lowercase, tokenize, remove punctuation and stopwords).
- Builds bigram and trigram models using `FreqDist` and `ConditionalFreqDist`.
- Predicts the next word and generates word sequences.

### Exp 5 (Part 2) – N-gram Model with Reuters Corpus & Perplexity
- Trains a trigram model on the NLTK **Reuters** corpus.
- Predicts the next word from two previous words.
- Calculates **perplexity** to evaluate the language model.

### Exp 6 – POS Tagging
- POS tagging using NLTK's built-in tagger.
- Training **Unigram** and **Bigram** taggers (with backoff) on the Treebank corpus.
- Evaluating accuracy (Unigram ≈ 96.01%, Bigram ≈ 98.52%).

### Exp 7b – Named Entity Recognition (NER)
- POS tagging followed by `ne_chunk` in NLTK.
- NER using **spaCy** (`en_core_web_sm`).
- Comparison of NLTK and spaCy entity labels (PERSON, GPE, CARDINAL, etc.).

### Exp 8 – TF-IDF & Cosine Similarity
- Converts documents into TF-IDF vectors using `TfidfVectorizer`.
- Finds similarity between documents using cosine similarity.

### Exp 9 – Word Sense Disambiguation (Lesk Algorithm)
- Implements the **Lesk algorithm** using WordNet definitions and examples.
- Finds the correct sense of an ambiguous word (e.g. "bank") from its sentence.
- Evaluates accuracy on a small dataset.

### Exp 10 – Exploratory Text Analysis on IMDb Reviews
- Loads the IMDb dataset (`stanfordnlp/imdb`) from Hugging Face.
- Checks missing values and duplicates, computes text statistics.
- Cleans text, plots review length distribution and top words.
- Removes stopwords, generates a word cloud and performs bigram analysis.

---

## Libraries Used
`nltk` · `spacy` · `scikit-learn` · `pandas` · `matplotlib` · `wordcloud` · `datasets` · `emoji` · `svgling`

## How to Run
1. Open any `.ipynb` file in **Google Colab** or Jupyter Notebook.
2. Install the required libraries if needed:
   ```bash
   pip install nltk spacy scikit-learn pandas matplotlib wordcloud datasets emoji svgling
   python -m spacy download en_core_web_sm
   ```
3. Run all cells in order (`Runtime → Run all` in Colab).
4. The required NLTK data (punkt, stopwords, wordnet, etc.) is downloaded inside the notebooks.
