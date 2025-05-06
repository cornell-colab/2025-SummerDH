---
layout: page
subheadline: "June 12, 2025"
title: "Word Embeddings"
teaser: ""
header: no
permalink: "/text/day9/"
---

## TEXT: Word Embeddings and Topic Modeling

## Before the session:

### Reading: Word Emebddings
* ["Understanding and Creating Word Embeddings"](https://programminghistorian.org/en/lessons/understanding-creating-word-embeddings) (Blankenship et al., 2024):
  Just read the ["Theory: Introducing Concepts" section](https://programminghistorian.org/en/lessons/understanding-creating-word-embeddings#theory-introducing-concepts), from "Word Embeddings" through "Vector Math." 

### Readings: Topic Modeling
* [Topic Modelling](https://melaniewalsh.github.io/Intro-Cultural-Analytics/05-Text-Analysis/06-Topic-Modeling-Overview.html) (Walsh, 2021)
* "[what is topic modeling and for whom is this useful?](https://programminghistorian.org/en/lessons/topic-modeling-and-mallet#what-is-topic-modeling-and-for-whom-is-this-useful)" section in [Introduction to Topic Modeling and MALLET](https://programminghistorian.org/en/lessons/topic-modeling-and-mallet) (Graham et. al, 2021)
  
* Walsh, Melanie, and Maria Antoniak. “[The Goodreads ‘Classics’: A Computational Study of Readers, Amazon, and Crowdsourced Amateur Criticism](https://post45.org/2021/04/the-goodreads-classics-a-computational-study-of-readers-amazon-and-crowdsourced-amateur-criticism/).” Post45: Peer Reviewed, Apr. 2021. post45.org.

## During the session:

### Part One: Word Embeddings

1. Returning to Matt's slides yesterday

#### Key points:
* "A ‘vector’ is a point in space that has both ‘magnitude’ (or ‘length’) and ‘direction.’ This means that vectors are less like isolated points, and more like lines that trace a path from an origin point to that vector’s designated position, in what is called a ‘vector space.’ Models created with word vectors, called ‘word embedding models,’ use word vectors to capture the relationships between words based on how close words are to one another in the vector space." - Blankenship et al. 

* We can use count vector document-term matrices as a way to represent "sparse" vector representation. In this model, each row is a document and each column is a word. The presence of the word in the document is marked with binary values: 0 if the word does not occur in the text, 1 if it does.

* Example from [_Humanities Data Analysis: Case Studies with Python_](https://www.humanitiesdataanalysis.org/vector-space-model/notebook.html#chp-vector-space-model) (Kardsorp et al., 2021)
"Extracting a document-term matrix from a collection of texts."

![image](https://github.com/cornell-colab/2024-SummerDH/assets/95382014/31e90e45-5e3c-4e89-befb-7ad26c469e06)

* "Dense" vector representation means that there are more values in the word vector's dimensions.

* TF-IDF is technically a form of word vectorization. We might remember from the Walsh (2021) reading earlier this week:

"**tf-idf = term_frequency * inverse_document_frequency**

"**term_frequency = number of times a given term appears in document**

"**inverse_document_frequency = log(total number of documents / number of documents with term) + 1*****

"You take the number of times a term occurs in a document (term frequency). Then you take the number of documents in which the same term occurs at least once divided by the total number of documents (document frequency), and you flip that fraction on its head (inverse document frequency). Then you multiply the two numbers together (term_frequency * inverse_document_frequency).

"The reason we take the inverse, or flipped fraction, of document frequency is to boost the rarer words that occur in relatively few documents."

* Packages that support vector analyses:
  1. word2vec (gensim)
  2. NLTK
  3. scikit-learn

#### Differentiating between word embeddings and topic modeling

"Unlike topic models, which rely on word frequency to better understand the general topic of a document, word embeddings are more concerned with how words are used across a whole corpus." - Blankenship et al. (2024)


### Topic Modeling
* "Topic models are useful for understanding collections of texts in their broadest outlines and themes. If you wanted to get a sense of the primary subjects discussed in thousands of journal articles published over multiple decades, then topic modeling might be a good choice. Topic models can also be helpful for looking at the fluctuation of topics and themes over time (this is a time series approach that we will discuss in the next lesson) or finding clusters of texts that contain the same or similar topics." - Walsh (2021)

* Our discussions on topic modeling here center on latent diralecht allocation (LDA) topic modeling, as it is a widely common method.
* LDA topic modeling is an unsupervised algorithm, meaning the researchers do not give the model outside information or labeling to inform its processes. This also means that there is a bit of randomness to the results.
* "Topics" are the labels that the human researcher ascribes to a cluster of words that the topic model produces. Sometimes, these toipcs might not make sense and they might not seem helpful for better understanding the corpus. They are what we make of themm.

* Additional note about the randomness and inconsistency with results: This randomness and inconsistency is pronounced when running the model with a smaller number of topics (e.g., 10 topics for a large corpus will be much more inconsistent than 50 or 100 topics might be, for example). It can really depend on several factors including the size of one's corpus, the variations within the corpus one is working with, and the number of topics being run. Because of that inconsistency, there doesn't really seem to be a disciplinary agreement about how to validate the results of a topic modeling analysis for all cases. Practitioners I know have said that practically, they run the model until the topics tend to make sense to them and become more consistent (e.g., using a larger number of topics and noticing when the model produces comparable results). Discerning whether the topics makes sense depends on familiarity with the documents, so topic modeling results can be supported/triangulated with other forms of close reading analyses. Let's ask Andrea!

### Activity (12ish minutes)

jsLDA Topic Modeling Tool
* [Link to tool](https://mimno.infosci.cornell.edu/jsLDA/jslda.html)
* [README file for jsLDA topic modeling tool](https://github.com/mimno/jsLDA/blob/master/README.md)

## After the session
1. Last group reflection prompt of SDH! Continue your reflection and memoing practice as it makes sense to you. We can continue using Github to share resources with one another.
2. Have a great weekend! After our invdividual check-ins, we'll kick off next week with the start of coworking.
