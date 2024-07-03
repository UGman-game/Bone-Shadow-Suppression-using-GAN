# Bone-Shadow-Suppression-using-GAN

This project leverages Generative Adversarial Networks (GANs) to address the challenge of bone shadow suppression in medical images. The goal is to enhance the clarity of medical images by reducing bone shadows, which can obscure important details.

Approach
Data Preprocessing:

Image Loading: Load source (input) and target (ground truth) images from a dataset stored in Google Drive.
Image Resizing: Resize images to a fixed size (120x120 pixels) for uniformity.
Normalization: Normalize pixel values to the range [0, 1].
Model Architecture:

Generator: A convolutional neural network (CNN) that generates bone shadow-suppressed images from input images.
Discriminator: A CNN that distinguishes between real (ground truth) images and generated images.
GAN: Combines the generator and discriminator to form the complete GAN, which is trained end-to-end.
Training:

Loss Functions: Binary cross-entropy loss for both generator and discriminator.
Optimization: Adam optimizer with a learning rate of 0.001.
Batch Processing: Used multiprocessing for efficient batch processing of images.
Epochs: Trained the model for 50 epochs with a batch size of 4.
Evaluation:

Visualization: Displayed target and generated images during training to visually assess the model's performance.
Discriminator Predictions: Evaluated the quality of generated images using the discriminator's predictions.
Saving and Loading Models:

Saved the generator model architecture and weights to disk.
Provided functionality to load the saved model for future use.
Testing:

Preprocessed test images from a local directory.
Generated bone shadow-suppressed images using the trained generator.
Passed the generated images through the discriminator to classify them as "Shadow Suppression Detected" or "No Shadow Suppression Detected".
Results
Successfully trained a GAN to perform bone shadow suppression on medical images.
Achieved significant reduction in bone shadows, improving the visibility of critical details in medical images.
Usage
Training:

Prepare a dataset with source and target images.
Run the training script to train the GAN.
Monitor the training process through loss plots and generated images.
Testing:

Use the provided script to preprocess test images.
Generate bone shadow-suppressed images using the trained generator.
Classify the generated images using the discriminator.
This project demonstrates the application of GANs in medical image processing, specifically targeting the enhancement of image quality by suppressing bone shadows.
