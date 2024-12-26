# **EM-Algorithm-for-Image-Denoising-ML-Course**
Image denoising using the EM algorithm with Gaussian Mixture Models (GMMs) on MNIST patches, reconstructing clean images from corrupted ones.
---

This project implements the **Expectation-Maximization (EM) Algorithm** for denoising images corrupted by blurring and additive noise, using patches extracted from the MNIST dataset. The approach models the distribution of image patches as a **Gaussian Mixture Model (GMM)** and applies techniques from Regularization Inverse Problems to infer clean images from corrupted data.

---

## **Objective**
The primary goal of this project is to estimate clean versions of corrupted images by:
1. Modeling image patches as samples from a GMM.
2. Applying the EM algorithm to infer the parameters of the GMM.
3. Reconstructing the denoised images by leveraging the posterior distribution of the clean patches.


