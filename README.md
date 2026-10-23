# NLP

My notebooks from the NLP1 practical sessions (TPs) at EPITA, C2 to C6. Some are in French and some in English.

`TP_NLP1_C2.ipynb` is preprocessing on a few French sentences with spaCy and nltk: tokenization, n-grams, stop words, stemming, lemmatization and POS tags. At the end there are some regex to pull out an email address and French phone numbers.

`TP_NLP1_C3.ipynb` builds a count vectorizer and TF-IDF by hand and compares sentences with cosine similarity, with and without stop words. Then the same thing with sklearn, plus bigrams.

`TP_NLP1_C4.ipynb` is text classification with BoW or TF-IDF and naive Bayes, SVM or logistic regression. First intent detection on 1243 French questions from [wikit-ai/nlu-french-benchmark](https://github.com/wikit-ai/nlu-french-benchmark), where the best was TF-IDF + SVM with 0.89 accuracy. Then sentiment on tweets: naive Bayes gets 0.64 accuracy and logistic regression on unigrams and bigrams gets 0.72. Last one is 20 Newsgroups, 0.70 with naive Bayes and 0.71 with logistic regression.

`TP_NLP1_C5.ipynb` is topic modeling. Only the LSA part is done: 10 topics on the first 10k articles of a French news dataset, then t-SNE on the topic vectors. The LDA, gensim and k-means parts are still the empty template.

`TP_NLP1_C6.ipynb` is information retrieval on the Alloprof dataset with text matching, TF-IDF and BM25. It only has the instructions, there's no code in it.

## Data and setup

There's no requirements file. The notebooks need pandas, scikit-learn, matplotlib, nltk, spaCy and gensim, plus seaborn and gdown for C5. The spaCy models are `fr_core_news_sm`, `en_core_web_sm` and `fr_core_news_md`.

C4 downloads the intent data from GitHub and 20 Newsgroups through sklearn. The tweets are from the Kaggle competition [Tweet Sentiment Extraction](https://www.kaggle.com/competitions/tweet-sentiment-extraction/data) and aren't in the repo because of the competition license. To get them:

```sh
kaggle competitions download -c tweet-sentiment-extraction
unzip tweet-sentiment-extraction.zip -d tweet-sentiment-extraction
```

C5 downloads its csv from Google Drive with gdown in the first cell.
