# Neural-machine-translation-english-to-polish using Attention model and Bert 
I had done a translation from English to Polish language using 2 models

  1.) Encoder-Decoder with Attention
      First, I have to preprocess the text using regular expression and tokenize the sentence using TensorFlow preprocessing and add the start and end words to the target sentence so that decoder knows that where to end.
          in the model, I had used encoder-decoder with attention in encoder and decoder I had used lstm and in that, I had done 2 exp 
          1.)  with adam as an optimizer and callback-ReduceLROnPlateau 
          2.)  Rmsprop optimizer and callback-Earlystoping 
          with that both give 80% accuracy but rmsprop worked well and given good translation then adam optimizer experiment 
      
  2.) Bert pre-trained model
      In this first, I had to convert the data into tensor slices and then tokenize the sentences using bert pre-trained tokenizer 
          I had used English pre-trained-'uncased_L-12_H-768_A-12' 
          in this, I had built a bert model as an encoder and a transformer as a decoder and set hyperparameters as (num_layers=6, d_model=512, dff=1024, num_heads=8) and obtained loss 0.1575 after 11 epochs and after that, it was translating well equal to the attention model but if I write a long sentence for translating it was not performing well because I had used max_seq_length=50 due to computational issue yeah you can change this and all hyperparameter then for sure you can see the difference in loss and accuracy and yeah this will take some long time.
          
          
Data :- http://www.manythings.org/anki/
 
Refrences:-
https://github.com/livingmagic/nmt-with-bert-tf2, 
https://github.com/harshilpatel99/NMT_english2marthi, 
https://arxiv.org/abs/2002.06823
