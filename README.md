# Training-distributed-representatio-GloVe-and-Word2Vec

## Introduction

This work explains how to train two separate word embeddings (Word2Vec and GloVe) and then use them to accomplish data clustering using Kmean and PCA for dimension reduction. Finally, presents the outcomes and how compact the visualizations are. For embedding training, both embeddings are trained on Wikipedia data. After that the word embeddings are used on different dataset to obtain representation making them ready  for the clustering phase, two different datasets are obtained to compare the final clustering visualization: Wikipedia pages of people and PubMed abstracts. The work follows the following steps:
-	Text preprocessing and tokenization 
-	Word vectorization 
-	Kmeans clustering 
-	PCA Dimensionality reduction
-	Visualization
The data is preprocessed using the NLTK package, which removes English stop words and lemmatizes the words in the text. For clustering I used MiniBatchKMeans is a KMeans version. Mini batches are subsets of the input data that are sampled at random throughout each training cycle. These mini batches significantly minimize the amount of computing needed to get a local solution.

## Findings
Data visualization is a key part of Dimensionality reduction. Dropping the dimensionality to two or three allows us to visualize the data, which is accomplished using PCA. Results shows that if the word embedding training data and the input corpus are comparable or belong to the same domain, more matches will occur between tokens from the input data and the embedding.
-	More point values will be found in clusters.
-	Clusters will be closer together.
-	Clusters will become increasingly overlapping.
- In the event of distinct domains data input and word embedding, the opposite will occur.*
- Negative sampling is used by Word2Vec this produces cone-shaped clusters of words in the vector space, whereas GloVe's word vectors are more discrete in the space, allowing word2vec to compute quicker than GloVe.
