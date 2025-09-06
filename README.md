# SNLP Assignments 1–5: J054

## Assignment 1

### Part 1
- Use a pretrained **Word2Vec** model (e.g., `word2vec-google-news-300`).
- Pick any 5 words and find their most similar words.
- Perform vector arithmetic experiments (e.g., `king - man + woman ≈ queen`) with 2–3 new examples.

### Part 2
Build a **movie review sentiment classifier** using WordVectors.

- **Dataset:** [IMDb Reviews (50K)](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/data)  
- **Tasks:**
  1. Perform text EDA  
  2. Clean text (remove punctuation, stopwords, etc.)  
  3. Train models using:  
     - Pretrained Word2Vec embeddings  
     - Custom Skip-gram vectors  
     - Custom CBOW vectors  
     - Custom FastText vectors  
  4. Compare and tabulate performance  

---

## Assignment 2

### Part 1
Train sentiment classifiers using **GloVe embeddings** with RNNs.

- **Dataset:** [IMDb Reviews (50K)](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/data)  
- **Experiments:**
  1. GloVe + Vanilla RNN  
  2. GloVe + LSTM  
  3. Repeat with on-the-fly embeddings ([torch.nn.Embedding](https://pytorch.org/docs/stable/generated/torch.nn.Embedding.html))  


---

### Part 2
Build a **date parser** (rule-based, no ML).  

- **Dataset:** `date_parser_testcases.csv`  
- Extract `day/month/year` from text and output in `DD/MM/YYYY`.  
  - Example: *“I went to London on 21st June, 2024” → `21/06/2024`*  


---

### Part 3
Develop a **rule-based gender pronoun transformer**.  

- **Example:**  
  - Input: `"He gave her his book."` (target gender: female)  
  - Output: `"She gave him her book."`  

---

## Assignment 3
Fine-tune multiple models on IMDb dataset.

- **Dataset:** [IMDb Reviews (50K)](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/data)  
- **Tasks:**
  1. Finetune 5 different models on a subset of the data  
  2. Select the best-performing model  
  3. Train the best model on the full dataset  
  4. Use a **custom F1-score function** for evaluation  
  5. Run inference on 10 random test reviews  

---

## Assignment 4

### Task 1 – Query Matching
- **Files:** [Resolved Queries](resolved_queries.csv), [New Queries](new_queries.csv)  
- Match unresolved queries with resolved queries using:  
  - Fuzzy Search (experiment with methods + thresholds)  
  - BoW / TF-IDF with cosine similarity  

---

### Task 2 – Name Matching
- **Files:** [Base Names](base_names.csv), [Name Variations](name_variations.csv)  
- Match names across lists (handling misspellings, abbreviations, format variations) using fuzzy search.

---

## Assignment 5
Build **semantic search models** for detecting duplicate questions (Quora dataset).

- **Dataset:** [Quora Question Pairs](https://www.kaggle.com/competitions/quora-question-pairs/overview)  
- **Experiments:**
  1. Baseline with default model weights  
  2. Bi-Encoder with Cosine Similarity Loss  
  3. Bi-Encoder with Contrastive Loss  
  4. Bi-Encoder with Multiple Negatives Ranking Loss  
  5. Cross-Encoder  

- Keep the test set constant across all experiments  
- Use **F1-score** for model comparison  
