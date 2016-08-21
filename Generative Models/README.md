# Introduction
Deep neural networks have found their way to wide variety of applications but only recently has the application of these networks for unsupervised and semi supervised learning leveraging large unlabeled data has been worked upon.

Generative modeling is a branch of machine learning that attempts at modeling the probability distribution of high dimensional data, for example - images.  Images present themselves as high dimensional data points that are mostly correlated. Take for instance a character image specifically say digits 0-9. It is highly unlikely that given the left half of the image contains the left half of 0; the right half would contain the left half of say 5. The generative models job is to capture these kinds of dependencies between pixels. In case of images by training a model to generate images as real as possible or as close to the actual dataset as possible is a good way to capture these dependencies.

### Hidden/ Latent Variables
Intuitively say we have a vector of latent variable **z** and assuming we can find a function f(**z**, **θ**) where **θ** is a vector of parameters. Now, training a generative model is to define this function such that for every data point **X** in our dataset, there is one setting of the latent variables which is able to generate something very similar to **X**. By being able to obtain such a function we have found the underlying/ defining low dimension space – which can be potentially used for various other tasks like classification, clustering and such.

### Auto Encoders
Auto Encoder is a methodology which tries to learn a function f(**X**| **θ**) = **X**, i.e an identity mapping. Seems like a trivial task, but by forcing specific constrains such as compressing the input from high dimension to lower dimension and then reconstructing we can discover interesting structure in data if one exists. In fact a simple auto encoder can learn features similar to a principal component analysis. Auto encoders have recently received attention with the advent of neural networks that have proved to be very good function approximators and their ability to encode information efficiently. Training auto encoders is theoretically nothing but a maximum likelihood technique to learn a function.
Several improvements to the basic auto encoder are being studied and applied. These improvements are primarily enforced by adding additional constrains like sparsity on the latent dimension space (Sparsity auto encoders) or by defining different loss function to train the network on for e.g. by using Kullback Leibler divergence term in the loss we can train a network with strong distribution prior on the latent variables (Variational Auto encoder). 

### Generative Adversarial Networks
Generative adversarial networks are methods that are based on game theory. The idea is to have two networks
 - Generator network G(**z**| **θ**) that produces samples from the data distribution by transforming a noisy vector **z**. 
 - Discriminator network D(**X**) that tries to differentiate a real data point from that which was generated. 

By jointly training these two networks to play a cat and mouse game we hope to achieve a representation that is useful to describe the dataset.
GAN are very unstable to train and so require careful selection of model activations and the model itself. The problem is mainly due to the fact that the optimization techniques used for training these networks are not meant for finding Nash equilibrium which is the ideal point where we want the networks to be at after training.

# Experiments
...to be updated.

