# Generative-model-using-PyTorch

One of the most interesting parts of GANs is the design of the **Generator**. The Generator network is able to take random noise and map it into images such that the discriminator cannot tell which images came from the dataset and which images came from the generator.

This is a very interesting application of neural networks. Typically neural nets map input into a binary output, (1 or 0), maybe a regression output, (some real-valued number), or even multiple categorical outputs, (such as MNIST or CIFAR-10/100).

DCGAN is one of the popular and successful network design for GAN. It mainly composes of convolution layers without max pooling or fully connected layers. It uses convolutional stride and transposed convolution for the downsampling and the upsampling. The figure below is the network design for the generator.

Here is the summary of DCGAN:

Replace all max pooling with convolutional stride
Use transposed convolution for upsampling.
Eliminate fully connected layers.
Use Batch normalization except the output layer for the generator and the input layer of the discriminator.
Use ReLU in the generator except for the output which uses tanh.
Use LeakyReLU in the discriminator.
