# README

## Project: Enhancing NeRF Model

This project focuses on enhancing the NeRF (Neural Radiance Fields) model by exploring improvements through model modifications and image preprocessing. Our goals include improving the quality of 3D scene reconstructions and understanding how different loss functions, model architectures, and contrast adjustments impact the results.

### 1. Dataset Preparation

Due to constraints in capturing our own dataset, we are using the synthetic dataset provided by the original NeRF authors.

### 2. NeRF Research

A targeted literature review was conducted to identify advancements in NeRF technology by examining papers citing the original NeRF work. This helped categorize potential modifications into two areas:

#### a) Model Modification

Several approaches were considered and implemented to improve the NeRF model:

1. **Different Loss Functions:**

   - **Huber Loss**
   - **Log Cosh Loss**
   - **Structural Similarity Index (SSIM) Loss**

2. **Model Architectures:**

   - Model with 2 layers & 128 filters, trained for:
     - 10k iterations
     - 100k iterations
   - Model with 8 layers & 256 filters, trained for:
     - 10k iterations
     - 100k iterations

3. **Distillation Approach:**
   - **Student:** Model with 2 layers & 128 filters, trained for 10k iterations
   - **Teacher 1:** Model with 8 layers & 256 filters, trained for 10k iterations
   - **Teacher 2:** Model with 8 layers & 256 filters, trained for 100k iterations

#### b) Image Preprocessing

1. **Increasing Image Contrast:**
   - Adjusted contrast using the formula `enhanced_image = original_image * gain + bias`.
