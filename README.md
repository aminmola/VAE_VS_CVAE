# VAE_VS_CVAE

This repository contains implementations and a comparative analysis of Variational Autoencoders (VAE) and Conditional Variational Autoencoders (CVAE). These are generative models capable of learning latent representations of input data and generating new data samples. The key difference between the two models lies in their ability to incorporate additional information (conditions) in the case of CVAE.

1. Variational Autoencoders (VAE)

A Variational Autoencoder (VAE) is a generative model that learns a probability distribution over the latent space of data. It encodes the input data into a latent space using a probabilistic approach and then samples from this latent space to reconstruct the original input.

* Encoder-Decoder Architecture: The encoder maps the input to a latent space, and the decoder reconstructs the input from this latent representation.
* Latent Space: The latent variables follow a Gaussian distribution. The encoder predicts the mean (μ) and standard deviation (σ) of this distribution.
* Reparameterization Trick: Used to allow backpropagation through the stochastic sampling process by parameterizing the sampling with a differentiable function.
* Loss Function: Combines the reconstruction loss (difference between input and output) with a KL divergence term (regularization that forces the latent space to follow a Gaussian distribution).

  
![alt text](<VAE.png>)


2. Conditional Variational Autoencoders (CVAE)

A Conditional Variational Autoencoder (CVAE) extends the VAE by incorporating conditional information in both the encoder and decoder. This allows for generating data conditioned on some auxiliary information (e.g., class labels), thus enabling controlled data generation.

* Conditioning Information: Additional input (such as labels or features) is provided to both the encoder and decoder to influence the latent space and generation process.
* Conditional Latent Space: The latent variables are conditioned on the input features or labels, allowing the model to generate specific outputs based on those conditions.
* Loss Function: Similar to VAE, CVAE optimizes a combination of reconstruction loss and KL divergence, but the loss is conditioned on the given information.

![alt text](<CVAE.png>)
