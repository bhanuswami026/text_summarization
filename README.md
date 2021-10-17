# TEXT-SUMMARIZATION:

### ABOUT TEXT SUMMARIZATION:

Text summarization is the concept of employing a machine to condense a document or a set of documents into brief paragraphs or statements using mathematical methods. NLP broadly classifies text summarization into 2 groups:
![alt text](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/13.jpg)

1] Extractive text summarization: here, the model summarizes long documents and represents them in smaller simpler sentences. 
![alt text](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/extractive1.jpg)

2] Abstractive text summarization: the model has to produce a summary based on a topic without prior content provided.
![alt text](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/abstractive1.jpg)

##### BERT-SUM USED FOR EXTRACTIVE TEXT SUMMARIZATION:
The input format of BERTSUM is different when compared to the original BERTSUM model. Here, a [CLS] token is added at the start of each sentence in order to separate multiple sentences and to collect features of the preceding sentence. There is also a difference in segment embeddings. In the case of BERTSUM, each sentence is assigned an embedding of Ea or Eb depending on whether the sentence is even or odd. If the sequence is [s1,s2,s3] then the segment embeddings are [Ea, Eb, Ea]. This way, all sentences are embedded and sent into further layers. 

BERTSUM assigns scores to each sentence that represents how much value that sentence adds to the overall document. So, [s1,s2,s3] is assigned [score1, score2, score3]. The sentences with the highest scores are then collected and rearranged to give the overall summary of the text. 


