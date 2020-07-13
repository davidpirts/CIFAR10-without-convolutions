# CIFAR10-without-convolutions

One can fairly straightforwardly achieve higher than 90% accuracy on the MNIST---and even Fashion MNIST---datasets, using neural networks with dense layers only. The 
collection of images in the CIFAR-10 dataset is famously much harder to classify *without convolutional layers*. Barring data augmentation, but invoking elaborate
tricks such as pretraining with autoencoders, the state of the art accuracy (as of five years ago) has been reported to lie around 63% in [this paper
from 2015](https://arxiv.org/abs/1511.02580). 

<img src="https://github.com/dprugby/CIFAR10-without-convolutions/blob/master/selu.png" align="right" width="400">

In this repository, we explore how feedforward networks of various depth (1, 2, 20 hidden layers) perform on the 
CIFAR-10 dataset *without* extra adjustments such as unsupervised pretraining. (Among the deep networks considered are the so-called self-normalizing feedforward  nets that overcome the vanishing/exploding gradients problem without batch normalization -- this is nicely illustrated with the help of TemsorBoard in the image to the right.)

After experimenting with different configurations, we (quite expectedly) conclude that 
the medium-depth dense networks perform best -- the one with 2 hidden layers achieves 55% validation accuracy. Deeper networks---in the present case, the one with 20 hidden layers---do not help performance much, only introducing extra standard issues such as higher rates of overfitting and vanishing gradients problems (with the exception of self-normalizing nets, of course). Taking care of the latter issues leads to significantly longer training times. 


