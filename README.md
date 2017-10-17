# udacity_dlnd_p3_languagetranslation
udacity_dlnd_p3_languagetranslation

## Project Overview
In this project, I took a peek into the realm of neural network machine translation. I was training a sequence to sequence model on a dataset of English and French sentences that can translate new sentences from English to French.

## Steps:

1. Preprocessing
    * Text to Word ids

2. Check the version of TensorFlow

3. Building the Network
    * model_inputs
    * process_decoding_input
    * encoding_layer
    * decoding_layer_train
    * decoding_layer_infer
    * decoding_layer
    * seq2seq_model

4. Training
    * Tuning parameters
        * Set epochs to the number of epochs.
        * Set batch_size to the batch size.
        * Set rnn_size to the size of the RNNs.
        * Set num_layers to the number of layers.
        * Set encoding_embedding_size to the size of the embedding for the encoder.
        * Set decoding_embedding_size to the size of the embedding for the decoder.
        * Set learning_rate to the learning rate.
        * Set keep_probability to the Dropout keep probability
        
5. Translate
	```python
	Input
	Word Ids:      [30, 64, 143, 170, 129, 200]
	English Words: ['he', 'saw', 'a', 'yellow', 'lemon', '.']

	Prediction
	Word Ids:      [177, 252, 293, 246, 108, 72, 180, 173, 1]
	French Words: ['il', 'est', 'le', 'terrain', 'de', "l'", 'automne', '.', '<EOS>'] 
	```

## Imperfect Translation
You might notice that some sentences translate better than others. Since the dataset was used only has a vocabulary of 227 English words of the thousands that could be used, the good results could be saw if only these words were used. Additionally, the translations in this data set were made by Google translate, so the translations themselves aren't particularly good.
Thankfully, for this project, a perfect translation was not really needed. However, if I want to create a better translation model, I'll need better data.
