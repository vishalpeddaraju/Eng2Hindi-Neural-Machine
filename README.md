# Eng2Hindi-Neural-Machine
The Model translator English to Hindi with the help of LSTM.The project was carried out using the Kersas framework. The English sentences were encoded into feature vectors that could be trained on, and the resulting vector was decoded back into the original Hindi text.

##Dataset
There are 62060 English phrases in the dataset, along with their Hindi translations. News portals, technical blogs, TED speeches, etc. are the areas where data is collected.

##The Model's construction parameters
*Establish a dictionary for both the input and output languages; 
*Create embedding matrices.
**The encoder and decoder models must be developed.
**GloVe embedding’s is used here. the 100-dimensional GloVe embedding’s of 400k words computed on an English Wikipedia dump from 2014. 
*make a dense layer for it.
*The input language from the training set.
*Display the predicated output 

##Model 
*In our model the common Seq2Seq learning frame work is being used with Encoder decoder.
*The key benefit of using Encoder Decoder model is, It can train a single End-To-End model directly on source and target sentences and the ability to handle variable length of input and output sequence text.

###Encoder
Encoder takes the English data as input and converts it into vectors that is passed to an LSTM model for training. 
	
###Decoder
  The Decoder use’s this internal representation to output words until the end of sequence of tokens is reached
  
  *LSTM is used for both encoder and decoder.

##Training 
*Google Collab was the platform utilised to construct the model, which was trained using LSTM. After training it around 2-3 times without resetting the weights and ruining it for 100 epoch at a time, which took about 2-3 hours, I was finally able to achieve an accuracy of 70%.
*RMS prop optimizer and Cross Entropy loss have both been employed. The model received the data in batches of 128.
