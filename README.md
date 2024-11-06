# GAN Training on CIFAR-10 Dataset

This project trains a Generative Adversarial Network (GAN) on the CIFAR-10 dataset using TensorFlow and Keras. The GAN architecture includes a generator that creates images from random noise and a discriminator that evaluates the authenticity of generated images. The project visualizes progress by saving generated images at each training epoch and creating an animated GIF to observe image quality improvements over time.

## Project Structure

- **Dataset Loading and Preprocessing**: CIFAR-10 dataset images are loaded and normalized to values between -1 and 1.
- **GAN Architecture**: The GAN model includes:
  - **Generator**: Takes a random noise vector as input and generates 32x32x3 images.
  - **Discriminator**: Classifies images as real or fake.
- **Training Functions**: Implements separate loss functions for the generator and discriminator, optimizing both with gradient descent.
- **Visualization Functions**: Generates and displays sample images from the generator after each epoch. A GIF is created to track training progress.

## Requirements

- Python 3.x
- TensorFlow
- Matplotlib
- ImageIO

## Setup and Execution

1. **Install Dependencies**:
    ```bash
    pip install tensorflow matplotlib imageio
    ```

2. **Run the Training**:
    The GAN model is trained on the CIFAR-10 dataset for a specified number of epochs.
    ```python
    train(train_dataset, epochs=1000)
    ```

3. **View Generated Images**:
    Each epoch saves a PNG file of the generated images in `/kaggle/working/`.

4. **Generate and Display Progress GIF**:
    After training, create a GIF from the generated images.
    ```python
    create_gif_from_images(num_epochs=10)
    ```

## Key Code Functions

- **display_sample_images**: Shows a 5x5 grid of images from the CIFAR-10 dataset.
- **make_generator_model**: Defines the generator model architecture.
- **make_discriminator_model**: Defines the discriminator model architecture.
- **generator_loss** and **discriminator_loss**: Define separate loss functions.
- **train_step**: One training step that updates generator and discriminator weights.
- **generate_and_save_images**: Saves generated images after each epoch.
- **create_gif_from_images**: Creates a GIF from saved images to visualize training progress.

## Output

- **PNG Images**: Generated images are saved after each epoch in the working directory.
- **GIF Animation**: A GIF showing progress over time is saved as `progress.gif`.

