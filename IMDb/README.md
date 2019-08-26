IMDb Dataset
The large movie review dataset contains 25,000 highly-polar movie reviews for training and the same amount again for testing. The problem is to determine whether a given movie review has a positive or negative sentiment.

Data source: http://ai.stanford.edu/~amaas/data/sentiment/

To be noted:

1. Words are already tokenized and converted to integers where the integers represent frequency in the dataset.
get_word_index() function is used to obtain the index:word dictionary.

2. The integers are mapped to a real valued vector of length 32 using an Embedding layer.

3. We train an LSTM model to classify the sequences. It can choose which words are crucial and which are to be forgotten    while    processing the data. To know more about the concept of LSTMs, refer to this article(https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21).

4. LSTM carries a risk of overfitting. So to decrease the trend in convergence and thus combat overfitting, we apply dropout in the input and the recurrent connections of the memory unit. 






