# pytorch-tutorial

## Tutorial 1 - October 21, 2022
In this tutorial we will cover installation of PyTorch, Tensor basics and how to train your first neural network (MLP; multi-layer perceptron) in order to classify hand-written digits (aka MNIST dataset).
The aim is get our feet wet and hands dirty in the world of deep learning. Each tutorial will work to cover increasingly complex topics as well as best practices. 

## Tutorial 2 - October 27, 2022
In this tutorial we will begin to move into more "atypical" neural networks. We begin by training a Variational AutoEncoder (VAE) https://arxiv.org/pdf/1906.02691.pdf. VAE's are generative models that comprise of 2 components, an encoder and a decoder. The encoder maps the inputs (data) to a lower-dimensional embedding/latent space. In fact, for each input, 2 different vectors are mapped to the lower-dimensional embedding space - one representing a multivariate normal mean, and one representing the diagonal entries of a multivariate gaussian covariance matrix. Hence, each data instance is mapped to the sufficient statistics of a multivariate normal distribution. The decoder uses these sufficient statistics to sample from this distribution (multivariate normal with mean and covariance produced from the encoder), and reconstructs the original input. Once sufficiently trained, the encoder can be discarded and one can sample random vectors from multivariate normal distributions, use these as inputs into the decoder, and produce synthetic data (thus generative model).

Second, we will cover a neural network that takes 2 separate inputs, and produces 3 separate outputs. The model is trained with 3 different losses. Concretely, we will use the MNIST dataset (images of hand written digits) to have 2 separate images used as the inputs, and the model will be trained to recognize the digit (class) of each image, and then perform addition. Let's teach machines how to do addition! Moreover, we will explore building our own custom dataset object, since each batch will require more than just a set of inputs and a set of labels.

