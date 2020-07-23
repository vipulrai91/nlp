
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
