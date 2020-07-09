# CIFAR10-without-convolutions

One can fairly straightforwardly achieve higher than 90% accuracy on the MNIST---and even Fashion MNIST---datasets, using neural networks with dense layers only. The 
collection of images in the CIFAR-10 dataset is famously much harder to classify *without convolutional layers*. Barring data augmentation (but invoking elaborate
tricks such as pretraining with autoencoders), the state of the art accuracy (as of five years ago) was reported to lie around 63 % in [this paper
from 2015](https://arxiv.org/abs/1511.02580). In this repository, we explore how feedforward networks of various depth (1, 2, 20 hidden layers) perform on the 
CIFAR-10 dataset without extra adjustments such as unsupervised pretraining. After experimenting with different configurations, we (quite expectedly) conclude that 
the medium-depth networks perform best -- the dense network with 2 hidden layers achieves 55 % validation accuracy in our case. 
