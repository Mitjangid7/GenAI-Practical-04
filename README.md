# Practical No. 04: Image Generation using Deep Convolutional GAN (DCGAN)

## Student Information

- **Name:** Mit Jangid
- **PRN:** 202401110072
- **Batch:** A1
- **Subject:** Generative AI

## Aim

To implement and train a Deep Convolutional Generative Adversarial Network (DCGAN) on a standard image dataset, generate synthetic images using the trained model, and evaluate its performance by analyzing Generator and Discriminator loss curves and generated image quality.

## Dataset

This implementation uses the **MNIST handwritten digit dataset**.

- Image size: 28 × 28 pixels
- Image type: Grayscale
- Original training dataset: 60,000 images
- Images used for training: 20,000 (reproducible subset)
- Number of classes: 10 (digits 0–9)

The images are normalized to the range [-1, 1] before training.

## Model Architecture

### 1. Generator
- Takes a 64-dimensional random noise vector as input.
- Uses a Dense layer and reshaping operation.
- Uses Conv2DTranspose layers for image upsampling.
- Uses Batch Normalization and ReLU activation.
- Produces a 28 × 28 grayscale synthetic image using tanh activation.

### 2. Discriminator
- Takes a 28 × 28 grayscale image as input.
- Uses convolutional layers for feature extraction.
- Uses LeakyReLU activation and Dropout.
- Uses a Dense output layer to classify real and generated images.

## Training Configuration

| Parameter | Value |
|---|---|
| Dataset | MNIST |
| Training subset | 20,000 images |
| Latent dimension | 64 |
| Batch size | 128 |
| Epochs | 15 |
| Optimizer | Adam |
| Learning rate | 0.0001 |
| Beta 1 | 0.5 |
| Framework | TensorFlow / Keras |

## Implementation Workflow

1. Import libraries and set random seeds.
2. Load and preprocess the MNIST dataset.
3. Build the Generator network.
4. Build the Discriminator network.
5. Define Generator and Discriminator loss functions.
6. Configure separate optimizers.
7. Train both networks using adversarial training.
8. Generate synthetic images at selected epochs.
9. Plot Generator and Discriminator loss curves.
10. Save trained models and loss history.

## Evaluation

The DCGAN is evaluated using:

- Generator loss curve.
- Discriminator loss curve.
- Visual quality of generated images.
- Comparison of generated samples across training epochs.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Google Colab

## Repository Contents

- `Mit_Jangid_DCGAN_MNIST_Practical_04.ipynb` – Complete implementation with code and outputs.
- `README.md` – Practical documentation.

## Conclusion

A Deep Convolutional Generative Adversarial Network was implemented using MNIST handwritten digit images. The Generator learns to create synthetic digit images, while the Discriminator learns to distinguish real images from generated ones. The training process is analyzed through Generator and Discriminator loss curves and visual inspection of generated images.

## Author

**Mit Jangid**  
TY AIML | Batch A1
