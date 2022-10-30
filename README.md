# Topic analysis

## LDA

### Benefits

- one document can have multiple topics
- performs better on smaller datasets

### Preprocessing

This model needed preprocessing in order to work. For this, I used the open source library spacy and nltk. I removed stopwords, punctuations, numbers, special characters and lemmatized all words. Additionally, I removed contractions such as "I'm" -> "I am"

![](images/wordcloud.png)

### Training

For the training process, I used the LdaMulticore model from gensim. The training process is very fast, but needed a specified amount of topics to find.

### Results

To visualize the results, I used the open source library "pyLDAvis". The interactive version of the visualisation can be viewed at "./results/ldavis_prepared_4.html". 

But the resulting topics were underwhelming and at no point meaningful. This is probably caused by the lack of data. There was a general overrepresentation of broad words like "quarter" and "think" in all topics.

![](images/LDA.png)

## Top2Vec

### Benefits

- Embedding based

- Deeper understanding of content

### Preprocessing

The Top2Vec model includes all preprocessing, so there is no need to do it yourself.

### Training

Training the Top2Vec model is as simple as writing one line. For better performance, I used a pretrained sentence encoder.

![](images/Top2Vec.png)

### Results

The results of the Top2Vec model were a lot closer to what I have expected. There was a clear seperation of the documents by topic (4 found by the model -> represents the 4 companies). 

![](images/topic_2.png)

![](images/topic_3.png)

## Credits

All code was developed by Moritz Enderle.
