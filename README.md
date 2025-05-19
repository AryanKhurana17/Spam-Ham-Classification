# Spam Detection using NLP and Word2Vec

## Project Overview
This project implements a spam/ham email classifier using Natural Language Processing (NLP) techniques.
The main focus is on preprocessing raw email text data and building machine learning models with different
text vectorization methods including Bag of Words (BoW), TF-IDF, and a custom-trained Word2Vec model.

## Dataset
The dataset contains email messages labeled as 'spam' or 'ham' with two columns:
- **label**: Indicates whether the email is spam or not.
- **message**: The raw email text.

## Project Steps
1. **Data Preprocessing**  
   - Train-test split to avoid data leakage  
   - Text cleaning (removal of non-alphabet characters, lowercasing)  
   - Tokenization and stopword removal  
   - POS tagging and lemmatization for better normalization  
   - Creation of a cleaned corpus for vectorization  

2. **Feature Extraction Methods**  
   - Bag of Words (BoW)  
   - TF-IDF  
   - Word2Vec embeddings trained from scratch using gensim  

3. **Modeling**  
   - Multinomial Naive Bayes for BoW and TF-IDF features  
   - SVC using Word2Vec averaged embeddings  

4. **Evaluation**  
   - Accuracy, Precision, Recall, and F1-score metrics  
   - Comparison of different vectorization techniques  

## Results
- Achieved approximately **97.67% accuracy** with the Bow + Multinomial NB, outperforming TF-IDF and custom Word2Vec models.

## Key Insight:
- **BoW > TF-IDF** in this case because spam messages often repeat certain keywords (e.g., "free", "win", "money"), and BoW emphasizes frequency more directly than TF-IDF.

## Tools and Libraries
- Python 3.x  
- pandas, numpy  
- nltk (tokenization, stopwords, POS tagging, lemmatization)  
- gensim (Word2Vec training)  
- scikit-learn (vectorizers, classifiers, evaluation metrics)  
- matplotlib, seaborn (for EDA visualizatio)  

## How to Run
1. Clone this repository.  
2. Install required packages
3. Run the Jupyter notebook to reproduce preprocessing, training, and evaluation steps.

## Contact
Feel free to reach out for questions or collaboration:  
**Aryan Khurana** — aryankhurana1701@gmail.com  

