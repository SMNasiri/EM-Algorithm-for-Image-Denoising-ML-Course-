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

---

## **Features**
### **1. Data Preparation**
- Extract patches from images in the MNIST dataset with overlapping windows.
- Vectorize patches into 1D arrays and save them as a dataset for modeling.
- Experiment with various patch sizes (`m = 4, 8, 12, 16, 20, 28`) to identify the optimal size for denoising.

### **2. EM Algorithm for GMM**
- Assume patches follow a GMM with `K` components.
- Implement and fine-tune the EM algorithm to estimate the means and variances of the GMM.
- Perform cross-validation to determine the optimal number of components (`K`).

### **3. Denoising Algorithm**
- Model corrupted patches as samples from a conditional distribution, `pY|Z`, which accounts for blurring (via matrix `W`) and additive noise.
- Calculate the posterior distribution, `pZ|Y`, to infer clean patches.
- Reconstruct the denoised images by averaging overlapping patches.

### **4. Visualization and Results**
- Plot noisy images and their corresponding denoised versions.
- Experiment with hyperparameters (`K`, `m`, and noise variance `σ`) to optimize performance.
- Evaluate the effectiveness of the first-order MAP approximation for this problem.

---

## **Key Components**
1. **Data Preparation**:
   - Extract overlapping patches and vectorize them.
   - Save the processed patches in arrays for training and validation.

2. **Hyperparameter Tuning**:
   - Fine-tune patch size (`m`), number of GMM components (`K`), and noise variance (`σ`) using cross-validation.

3. **Posterior Approximation**:
   - Approximate the MAP estimate for the posterior `pZ|Y` by finding the component with the maximum probability.

4. **Image Reconstruction**:
   - Reconstruct denoised images by reshaping patches and averaging overlapping pixel values.

---

## **Simulation Questions Addressed**
1. **Patch Extraction**:
   - Extract patches from 1000 MNIST images and save them in a vectorized format.
2. **GMM Parameter Estimation**:
   - Use the EM algorithm to estimate the GMM parameters for the patches.
3. **Denoising Patches**:
   - Apply the MAP approximation to denoise patches and reconstruct images.
4. **Visualization**:
   - Compare noisy and denoised images, evaluating the effectiveness of the method.

