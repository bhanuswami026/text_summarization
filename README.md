# TEXT-SUMMARIZATION:

### WHY TEXT SUMMARIZATION?
Text Summarization is one of those applications of Natural Language Processing (NLP) which is bound to have a huge impact on our lives. With growing digital media and ever growing publishing – who has the time to go through entire articles / documents / books to decide whether they are useful or not? Thankfully – this technology is already here. Have you come across the mobile app inshorts? It’s an innovative news app that converts news articles into a 60-word summary. This app is based on text summarization.

### ABOUT TEXT SUMMARIZATION:

Automatic Text Summarization is one of the most challenging and interesting problems in the field of Natural Language Processing (NLP). It is a process of generating a concise and meaningful summary of text from multiple text resources such as books, news articles, blog posts, research papers, emails, and tweets.

Text summarization is the concept of employing a machine to condense a document or a set of documents into brief paragraphs or statements using mathematical methods. NLP broadly classifies text summarization into 2 groups:
![alt text](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/13.jpg)

1] Extractive text summarization: here, the model summarizes long documents and represents them in smaller simpler sentences. 
![alt text](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/extractive1.jpg)

2] Abstractive text summarization: the model has to produce a summary based on a topic without prior content provided.
![alt text](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/abstractive1.jpg)

#### BERT-SUM USED FOR EXTRACTIVE TEXT SUMMARIZATION:
The input format of BERTSUM is different when compared to the original BERTSUM model. Here, a [CLS] token is added at the start of each sentence in order to separate multiple sentences and to collect features of the preceding sentence. There is also a difference in segment embeddings. In the case of BERTSUM, each sentence is assigned an embedding of Ea or Eb depending on whether the sentence is even or odd. If the sequence is [s1,s2,s3] then the segment embeddings are [Ea, Eb, Ea]. This way, all sentences are embedded and sent into further layers. 

BERTSUM assigns scores to each sentence that represents how much value that sentence adds to the overall document. So, [s1,s2,s3] is assigned [score1, score2, score3]. The sentences with the highest scores are then collected and rearranged to give the overall summary of the text. 

#### EXTRACTIVE TEXT SUMMARIZATION BASED ON TEXTRANK:
Textrank algorithm takes its insipiration from google's pagerank algorithm. 

In text rank algorithm:
* Similarity between any two sentences is used as an equivalent to the web page transition probability
* The similarity scores are stored in a square matrix, similar to the matrix M used for PageRank

TextRank is an extractive and unsupervised text summarization technique. Let’s take a look at the flow of the TextRank algorithm that we will be following:
![alt text](https://cdn.analyticsvidhya.com/wp-content/uploads/2018/10/block_3.png)

#### SEQ2SEQ FOR ABSTRACTVE TEXT SUMMARIZATION:
We can build a Seq2Seq model on any problem which involves sequential information. This includes Sentiment classification, Neural Machine Translation, and Named Entity Recognition – some very common applications of sequential information. Our objective is to build a text summarizer where the input is a long sequence of words (in a text body), and the output is a short summary (which is a sequence as well). So, we can model this as a Many-to-Many Seq2Seq problem. 

There are two major components of a Seq2Seq model: 
* Encoder 
* Decoder
Both the parts are practically two different neural network models combined into one giant network.


Below is a typical Seq2Seq model architecture:
![alt text](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/final.jpg)

Broadly, the task of an encoder network is to understand the input sequence, and create a smaller dimensional representation of it. This representation is then forwarded to a decoder network which generates a sequence of its own that represents the output. 

The Encoder-Decoder architecture is mainly used to solve the sequence-to-sequence (Seq2Seq) problems where the input and output sequences are of different lengths. Generally, variants of Recurrent Neural Networks (RNNs), i.e. Gated Recurrent Neural Network (GRU) or Long Short Term Memory (LSTM), are preferred as the encoder and decoder components. This is because they are capable of capturing long term dependencies by overcoming the problem of vanishing gradient.
