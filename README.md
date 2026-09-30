# NLP — TPs (EPITA)

Notebooks des TPs du cours de Traitement du Langage Naturel (NLP1) : prétraitement, vectorisation,
classification de texte, topic modeling et recherche d'information.

| Notebook | Sujet |
|---|---|
| `TP_NLP1_C2.ipynb` | Prétraitement : tokenisation, stop words, stemming |
| `TP_NLP1_C3.ipynb` | Tokenizers et vectorisation |
| `TP_NLP1_C4.ipynb` | Classification de texte (détection d'intentions, sentiment sur tweets) |
| `TP_NLP1_C5.ipynb` | Topic modeling : LDA et LSA (spaCy, scikit-learn, Gensim) |
| `TP_NLP1_C6.ipynb` | Recherche d'information |

## Données

Le TP C4 utilise le dataset Kaggle
[Tweet Sentiment Extraction](https://www.kaggle.com/competitions/tweet-sentiment-extraction/data),
non inclus ici (licence de la compétition). Pour le récupérer :

```sh
kaggle competitions download -c tweet-sentiment-extraction
unzip tweet-sentiment-extraction.zip -d tweet-sentiment-extraction
```
