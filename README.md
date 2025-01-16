# Dogs-Cats-CNNs
Even though it is possible to build an entire neural network from scratch using only the PyTorch Tensor class, this is very tedious. And since most neural networks are based on the same building blocks, namely layers, it would make sense to generalize these layers as reusable functions. That is exactly what PyTorch provides with its torch.nn package.

The torch.nn package depends on autograd (as discussed in Part 2) to define the network models as well as to differentiate them (back-propagate). We usually define a new class for our model that extends class nn.Module. A nn.Module contains layers, as well as a methods forward(input) that returns a Variable which we will call output.

In the image below is the network we will build in this part, which we can use to classify hand written digits. We will use the popular MNIST dataset, which contains a training set of 60,000 labeled images and a test set of 10,000 labeled images.



It is a simple feed-forward convolutional neural network (CNN), which takes a 28 x 28 pixel, greyscale,  input image, that is then fed through several layers, one after the other, and finally gives an output vector, which contain the log probability (since we will use the Negative Log Likelihood loss function) that the input was one of the digits 0 to 9. I will not explain concepts like convolution, pooling or dropout in this post.
