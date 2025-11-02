# Wikipedia NLP Project

This project aims to perform **text preprocessing** and **visualization** on a dataset of Wikipedia articles using Natural Language Processing (NLP) techniques.  
The main goal is to clean, process, and analyze textual data to extract meaningful insights and visualize key terms using Python.

---

## Objective

Using Wikipedia text data to:
- Clean and normalize raw text,
- Remove unnecessary and low-frequency words,
- Perform lemmatization for linguistic normalization,
- Visualize the most frequent terms via **Barplots** and **WordClouds**.

---

## Task 1 — Text Preprocessing

### Step 1: `clean_text()` Function
A text-cleaning function was developed to:
- Convert all text to lowercase,  
- Remove punctuation and special characters,  
- Remove numeric values and excess whitespace.

### Step 2: Applying the Function
The `clean_text()` function was applied to the entire text column of the dataset.

### Step 3: Removing Stopwords
Stopwords (meaningless or redundant words) were removed using stopword lists in **English**, **French**, and **German** from the `nltk` corpus.

### Step 4: Removing Rare Words
Words appearing less than **1000 times** in the dataset were identified and removed.

### Step 5: Tokenization
Text was split into individual tokens (words) to allow further analysis.

### Step 6: Lemmatization
Each word was reduced to its root form using `TextBlob` and `Word` classes.

---

## Task 2 — Visualization

### Step 1: Word Frequency Calculation
Term frequencies (TF) were computed for all words in the cleaned dataset.

### Step 2: Frequency Barplot
The most frequent words were visualized using a **bar chart** to illustrate overall word importance.

### Step 3: WordCloud Generation
A **WordCloud** was created to display the most common terms visually, highlighting their relative frequencies by size.

---

## Task 3 — Combine All Steps into One Function

A single function named `wiki_nlp_wordcloud()` was created to execute all tasks sequentially.

### Example Usage:
```python
wiki_nlp_wordcloud(col='text')
