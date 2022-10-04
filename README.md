# Sentiment-Analysis

in this Notebbook ,We'll be using the  [Real or Not?](https://www.kaggle.com/c/nlp-getting-started/data)datset from Kaggle which contains text-based Tweets about natural disasters.

The Real Tweets are actually about diasters, for example:
"Jetstar and Virgin forced to cancel Bali flights again because of ash from Mount Raung volcano"

The Not Real Tweets are Tweets not about diasters (they can be on anything), for example:
'Education is the most powerful weapon which you can use to change the world.'

Since we have two target values, we're dealing with a binary classification problem.

Where,Our labels are in numerical form (0 and 1) but our Tweets are in string form .
* **1** = a real disaster Tweet
* **0** = not a real disaster Tweet

In **NLP**, there are two main concepts for turning text into numbers:
* **Tokenization** : A straight mapping from word or character or sub-word to a numerical value.
* **Embeddings** :An embedding is a representation of natural language which can be learned. Representation comes in the form of a feature vector. 

After we've got a way to turn our text data into numbers, we can build machine learning models to model it.

We'll be building the following models and comparing their performance:
* Model 1: Feed-forward neural network (dense model)
* Model 2: LSTM model
* Model 3: GRU model
* Model 4: Bidirectional-LSTM model
* Model 5: 1D Convolutional Neural Network
* Model 6: TensorFlow Hub Pretrained Feature Extractor
* Model 7: Same as model 6 with 10% of training data


![Screenshot (810)](https://user-images.githubusercontent.com/90212538/193794042-9f6fbeec-8272-4938-a3dc-c99e0045986d.png)

Looks like our pretrained USE TensorFlow Hub models have the best performance.

How about we find some Tweets and use USE TensorFlow Hub model to predict whether or not they're about a diaster or not?Such as the following two Tweets about the 2020 Beirut explosions.

**tweet1**
- Pred: 1.0 (real disaster) Prob: 0.9625465869903564
- Text:
Reports that the smoke in Beirut sky contains nitric acid, which is toxic. Please share and refrain from stepping outside unless urgent. #Lebanon


**tweet2**
- Pred: 1.0 (real disaster) Prob: 0.9678557515144348
- Text:
Beirut declared a “devastated city”, two-week state of emergency officially declared. #Lebanon

