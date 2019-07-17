# Generative-model-using-PyTorch

GANs biggest problem is that they are unstable to train (note the oscilations of the loss). This is due to the fact we train two networks from the same backpropagation. Also, we already know that we have better tools when it comes to image processing and deep learning – Convolutional Neural Networks (CNN). By combining main CNN concepts with GAN ideas, we can improve in this task and generate better images. That is how Deep Convolutional Generative Adversarial Network (DCGAN) were created.

One of the most interesting parts of GANs is the design of the **Generator**. The Generator network is able to take random noise and map it into images such that the discriminator cannot tell which images came from the dataset and which images came from the generator.

This is a very interesting application of neural networks. Typically neural nets map input into a binary output, (1 or 0), maybe a regression output, (some real-valued number), or even multiple categorical outputs, (such as MNIST or CIFAR-10/100).

DCGAN is one of the popular and successful network design for GAN. It mainly composes of convolution layers without max pooling or fully connected layers. It uses convolutional stride and transposed convolution for the downsampling and the upsampling. The figure below is the network design for the generator.

In order to stabilize GANs training, authors of DCGAN proposed several improvements:

- Utilizing the convolution layer instead pooling function in the Discriminator model for reducing dimensionality. This way, the network itself will learn how to reduce dimensionality. On the other hand, in the Generator Model, we use deconvolution to upsample dimensions of feature maps.
- Adding in the batch normalization. This is used to increase the stability of a neural network. In an essence, batch normalization normalizes the output of a previous layer by subtracting the batch mean and dividing by the batch standard deviation.
- Remove fully connected layers from Convolutional Neural Network.
- Use Relu and Leaky Relu activation functions.
