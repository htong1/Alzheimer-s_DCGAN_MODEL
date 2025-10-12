# Alzheimer-s_DCGAN_MODEL
Implemented a PyTorch-based DCGAN trained on Alzheimer’s MRI scans to synthesize brain images. Features convolutional generator and discriminator networks with batch normalization and latent vector sampling.

## Project Overview

This project implements a **Deep Convolutional Generative Adversarial Network (DCGAN)** in **PyTorch** trained on **MRI neuroimaging data** of Alzheimer’s patients.  
The goal is to generate **realistic synthetic brain scans** that mirror structural patterns of Alzheimer’s, providing potential data augmentation for deep learning applications in medical imaging.

### Key Features
- **Convolutional GAN architecture:** Generator uses transposed convolutions, batch normalization, and ReLU activations to produce 64×64×3 MRI images; Discriminator uses convolutions, batch normalization, and LeakyReLU for stable adversarial training.
- **Training pipeline:** Includes BCELoss, Adam optimizers, and monitoring of generator/discriminator loss dynamics.
- **Visualization:** Progress of generated images tracked using fixed latent vectors and `torchvision.utils.make_grid`.
- **Reproducibility:** Manual seeds and deterministic algorithms ensure consistent results across runs.
- **Custom dataset handling:** Dataset loader and preprocessing pipeline standardize MRI images for model input.

This project is my **second GAN implementation**, building on my first fully-connected GAN. I learned how **convolutional architectures and batch normalization** improve image realism and training stability for generative models, especially on complex neuroimaging data.

### Tools & Libraries
- **Python**, **PyTorch**, **Torchvision**, **Matplotlib**, **PIL**
- **Google Colab** for GPU training
- **MRI dataset** of Alzheimer’s patients and healthy controls

### Future Work
- Explore **conditional DCGANs** to control generated image features.
- Evaluate generated images with **quantitative metrics** such as FID or IS for quality assessment.
- Experiment with higher-resolution MRI data and multi-channel image synthesis for improved realism.
