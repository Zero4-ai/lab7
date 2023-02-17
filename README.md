# Lab7

## Learning Objective:
To model the low level image processing tasks in the framework of Markov Random Field and Conditional Random Field. To understand the working of Hopfield network and use it for solving some interesting combinatorial problems


## Reference:
http://www.cs.utoronto.ca/~strider/Denoise/Benchmark/
Interesting way to denoise an image using random walk: http://www.cs.toronto.edu/~fleet/research/Papers/BMVC_denoise.pdf
MRF Image Denoising: 
https://web.cs.hacettepe.edu.tr/~erkut/bil717.s12/w11a-mrf.pdf
Single Neuron and Hopfield Network: Chapter 40, 41, 42
Information Theory, Inference and Learning Algorithms, David MacKay
http://www.inference.phy.cam.ac.uk/mackay/itila/


## Problem Statement:

1. Many low level vision and image processing problems are posed as minimization of energy function defined over a rectangular grid of pixels. We have seen one such problem, image segmentation, in class. The objective of image denoising is to recover an original image from a given noisy image, sometimes with missing pixels also. MRF models denoising as a probabilistic inference task. Since we are conditioning the original pixel intensities with respect to the observed noisy pixel intensities, it usually is referred to as a conditional Markov random field.  Refer to (3) above. It describes the energy function based on data and prior (smoothness). Use quadratic potentials for both singleton and pairwise potentials. Assume that there are no missing pixels. Cameraman is a standard test image for benchmarking denoising algorithms. Add varying amounts of Gaussian noise to the image for testing the MRF based denoising approach. Since the energy function is quadratic, it is possible to find the minima by simple gradient descent. If the image size is small (100x100) you may use any iterative method for solving the system of linear equations that you arrive at  by equating the gradient to zero. Extra Credit Challenge: Implement and compare MRF denoising with Stochastic denoising (reference 2).

2. For the sample code hopfield.m supplied in the lab-work folder, find out the amount of error (in bits) tolerable for each of the stored patterns.

3. Solve a TSP (traveling salesman problem) of 10 cities with a Hopfield network.  How many weights do you need for the network?  
