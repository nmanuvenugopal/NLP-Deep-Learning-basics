Machine learning and deep learning algorithm needs to convert the plain text to numeric format for processing it. 

Word embeddings are a fundamental concept in natural language processing (NLP) that involve representing words as dense vectors in a continuous vector space. 
These vectors capture semantic relationships and contextual information between words, allowing machines to understand the meaning and relationships between words 
in a more meaningful way compared to traditional one-hot encoding or bag-of-words representations.

Here's why word embeddings are useful in NLP tasks:

1. Semantic Meaning: Word embeddings capture semantic meaning, which means that words with similar meanings are represented as vectors that are closer to each 
other in the embedding space. For example, in a good word embedding space, the vectors for "cat" and "dog" should be closer to each other than to words like "apple" 
or "car."

2. Contextual Information: Word embeddings take into account the context in which words appear. Words that often appear together in similar contexts will have 
similar vector representations. This is crucial for understanding word meanings in different contexts, such as the multiple meanings of the word "bank" in finance 
and geography.

3. Dimension Reduction: Word embeddings typically have lower dimensions compared to one-hot encoded representations or bag-of-words models. This reduces the 
dimensionality of the data, making computations more efficient and reducing the risk of overfitting.

4. Improved Performance: Many NLP tasks, such as sentiment analysis, machine translation, and named entity recognition, benefit from the use of word embeddings.
Models trained with word embeddings often achieve better performance because they can generalize better from the limited training data.

5. Out-of-Vocabulary Words: Word embeddings allow for handling out-of-vocabulary (OOV) words, which are words that are not present in the training data.
This is because embeddings provide continuous representations that can capture similarities even for words not seen during training.

6. Mathematical Operations: Word embeddings enable algebraic operations on words. For example, by subtracting the vector for "man" from "king" and adding the 
vector for "woman," you get a vector close to the word "queen." This showcases the ability to perform analogical reasoning with word embeddings.

7. Pretrained Models: Pretrained word embeddings, such as Word2Vec, GloVe, and fastText, are available for many languages and domains. These embeddings have
been trained on large text corpora and can be used as a starting point for various NLP tasks, saving time and resources.

8. Transfer Learning: Word embeddings facilitate transfer learning. A model pretrained on a large text corpus with word embeddings can be fine-tuned on a 
smaller dataset for a specific task, resulting in improved performance.


Word embedding can be classified into 2 types:
1. Frequency based embedding 
2. Prediction based embedding

Frequency-based and prediction-based embeddings are two approaches to creating word embeddings in natural language processing. These approaches differ in how they generate vector representations for words based on 
the analysis of large text corpora.

1. Frequency-Based Embedding:
   Frequency-based embeddings leverage the statistical properties of words in a text corpus, primarily based on the co-occurrence information of words within a certain context window. The underlying assumption is 
that words that frequently appear together in similar contexts are likely to have similar meanings.

Common frequency-based embedding methods include:
   
- Count-Based Methods (e.g., Term Frequency-Inverse Document Frequency, TF-IDF)**: These methods calculate a weight for each word based on its frequency in a document relative to its frequency in the entire corpus.
       While not exactly an embedding in the traditional sense, TF-IDF can be considered a frequency-based representation.
   
- Latent Semantic Analysis (LSA)**: LSA applies singular value decomposition (SVD) to a term-document matrix to capture latent semantic relationships between words.
   
 - Global Vectors for Word Representation (GloVe)**: GloVe constructs a co-occurrence matrix from the text corpus and uses matrix factorization to generate word embeddings that encode both global and local context 
information.
   
Frequency-based embeddings are often interpretable and can capture some aspects of word relationships, but they might struggle with capturing more complex semantic relationships and word analogies.

2. Prediction-Based Embedding:

Prediction-based embeddings involve training models to predict certain linguistic properties of words, given their context. These methods learn to capture the underlying structure of the language by optimizing the 
prediction task.

   Common prediction-based embedding methods include:
   
   - Word2Vec (Skip-gram and Continuous Bag-of-Words)**: Word2Vec models predict the likelihood of neighboring words given a target word or vice versa. Skip-gram predicts context words from a target word, 
     while Continuous Bag-of-Words predicts a target word from its context.
   
   - fastText: Building upon Word2Vec, fastText extends the prediction task to subword units (character n-grams), which is particularly useful for morphologically rich languages and handling out-of-vocabulary words.
   
   - Transformer Models (e.g., BERT, GPT)**: While initially designed for different tasks (BERT for masked language modeling, GPT for autoregressive language modeling), these models generate contextual embeddings that 
      have become highly effective for a wide range of NLP tasks.

   Prediction-based embeddings tend to capture complex semantic relationships better and can handle nuances such as word analogies, polysemy, and context-dependent meanings.
