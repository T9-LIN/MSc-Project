# MSc Project
**Project Title:** Chatbot as a conversational partner
**Student:** YONGFAN LIN

### Introduction

The goal of the project is to build a chatbot which can improve people's motivation and confidence to speak English.

An AI-based sound chatbot was built based on Pytorch framework and trained on the Cornell Movie-Dialogs Corpus.  


### Update

Upuload ``cornell_movie_dialogs_corpus.zip``  


### Prerequisites

python 3.6+

pytorch 1.2

pyttsx3 2.71

PyAudio 0.2.11

SpeechRecognition 3.8.1


### Installing

All packages can use pip to install

pip is already installed for Python 2 >=2.7.9 or Python 3 >=3.4 

``pip for Python 2``

```shell
$ pip install <package name>
```

``pip3 for Python 3``

```shell
$ pip3 install <package name>
```

### Corpus

**Cornell Movie--Dialogs Corpus**

This corpus contains a large metadata-rich collection of fictional conversations extracted from raw movie scripts:


```
- 220,579 conversational exchanges between 10,292 pairs of movie characters

- involves 9,035 characters from 617 movies

- in total 304,713 utterances

- movie metadata: genres, release year, IMDB rating, number of IMDB votes, IMDB rating

- character metadata: gender (for 3,774 characters), position on movie credits (3,321 characters)

```

### Architecture

At the heart of the AI-based chatbot is the Seq2Seq model, which has two independent recurrent neural networks, one for the encoder and the other for the decoder.

**Seq2Seq Model**

 ![image](https://jeddy92.github.io/images/ts_intro/seq2seq_ts.png 'The encoder-decoder architecture')

Image source: https://jeddy92.github.io/JEddy92.github.io/ts_seq2seq_intro/

**Encoder**

Encoders use the bidirectional variant of GRU to take advantage of past and future contexts.

 ![image](https://colah.github.io/posts/2015-09-NN-Types-FP/img/RNN-bidirectional.png 'Bidirectional RNN')

Image source: https://colah.github.io/posts/2015-09-NN-Types-FP/

**Decoder**

The decoder uses the Luong attention mechanism to generate an output based on the hidden state of all encoders, and only calculates the attention weights based on the hidden state of the decoder of the current time step.

 ![image](https://pytorch.org/tutorials/_images/global_attn.png 'Global attention mechanism')
 
Image source: https://arxiv.org/abs/1508.04025

### Acknowledgments

The chatbot borrows code from the Pytorch chatbot tutorial 

https://github.com/pytorch/tutorials/blob/master/beginner_source/chatbot_tutorial.py

The author is Matthew Inkawhich 

https://github.com/MatthewInkawhich


