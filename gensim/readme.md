
The core concepts of gensim are:

    Document: some text.

    Corpus: a collection of documents.

    Vector: a mathematically convenient representation of a document.

    Model: an algorithm for transforming vectors from one representation to another.


In Gensim, a **document** is an object of the text sequence type (commonly known as str in Python 3). A document could be anything from a short 140 character tweet, a single paragraph (i.e., journal article abstract), a news article, or a book.


A **corpus** is a collection of Document objects.

Corpora serve two roles in Gensim:
- Input for traiing the model. (Gensim focuses on unsupervised models so that no human intervention, such as costly annotations or tagging documents by hand, is required.)
- Documents to organize. After training, a topic model can be used to extract topics from new documents (documents not seen in the training corpus).

Eg : 

```python
text_corpus = [
    "Human machine interface for lab abc computer applications",
    "A survey of user opinion of computer system response time",
    "The EPS user interface management system"]
```

It consists of 3 documents, where each document is a string consisting of a single sentence.

**Vector**

To infer the latent structure in our corpus we need a way to represent documents that we can manipulate mathematically. One approach is to represent each document as a vector of features.

Vector can be represented in bag of words format where the vector representation would be unique coropus of the words at different index and the value would be it's frequency count.


**Model**

Now that we have vectorized our corpus we can begin to transform it using models.
We use model as an abstract term referring to a transformation from one document representation to another.


Simple Example using tf-idf

```python
from gensim import models

# train the model
tfidf = models.TfidfModel(bow_corpus)

# transform the "system minors" string
words = "system minors".lower().split()
print(tfidf[dictionary.doc2bow(words)])
```
