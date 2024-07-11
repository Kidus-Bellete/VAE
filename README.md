# FAVAE Anomaly Detection and Localization

This repository contains the implementation of Feature Augmented Variational Auto Encoder (FAVAE) for anomaly detection and localization. The FAVAE model leverages the power of variational autoencoders with enhanced feature augmentations to detect and localize anomalies in images.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Training](#training)
  - [Testing](#testing)
- [Directory Structure](#directory-structure)
- [Datasets](#datasets)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Anomaly detection and localization is crucial in various domains, such as industrial inspection, medical imaging, and security. This project utilizes a Variational Auto Encoder (VAE) architecture augmented with additional features to improve the performance of anomaly detection and localization.

The Feature Augmented Variational Auto Encoder (FAVAE) is an advanced deep learning model designed to tackle the challenges of anomaly detection and localization in image data. By combining the generative power of VAEs with enhanced feature extraction techniques, FAVAE offers several advantages over traditional approaches:

1. **Unsupervised Learning**: FAVAE can learn from normal data without requiring labeled anomalies, making it suitable for scenarios where anomalies are rare or unknown.

2. **Feature Augmentation**: Unlike standard VAEs, FAVAE incorporates additional feature extraction layers that capture both low-level and high-level image characteristics. This augmentation allows for more nuanced representation of normal patterns and better detection of subtle anomalies.

3. **Localization Capability**: In addition to detecting the presence of anomalies, FAVAE can pinpoint their location within the image. This is achieved through a novel reconstruction-based localization technique that highlights areas of high reconstruction error.

4. **Adaptability**: The model is designed to work with various types of image data, from simple textures to complex object arrangements, making it versatile for different industrial and scientific applications.

5. **Interpretability**: By visualizing the reconstructed images and localization maps, users can gain insights into why certain regions are flagged as anomalous, aiding in root cause analysis.

The FAVAE model is trained on a dataset of normal images, learning to compress and reconstruct them efficiently. During inference, it attempts to reconstruct test images. Anomalies are detected based on the reconstruction error, with higher errors indicating a higher likelihood of anomalous regions.

This implementation includes scripts for data preprocessing, model training, evaluation, and visualization of results. It's designed to be easily adaptable to different datasets and use cases within the domain of visual anomaly detection.

## Features

- Variational Auto Encoder with feature augmentations
- Unsupervised anomaly detection
- Pixel-wise anomaly localization
- Support for MVTec Anomaly Detection dataset
- Easy to use training and testing scripts
- Visualization tools for model outputs
- Flexible architecture for adaptation to various image types

## Installation

Clone this repository and install the required dependencies:

```bash
git clone https://github.com/Kidus-Bellete/VAE.git
cd VAE
pip install -r requirements.txt
```

## Usage

### Training

To train the FAVAE model, run:

```bash
python train.py --obj bottle --do_aug
```

You can adjust the training parameters in the `train.py` script.

### Testing

To test the trained FAVAE model, run:

```bash
python test.py
```

Results will be saved in the `results` directory.

## Directory Structure

```
FAVAE_Anomaly_Detection_And_Localization/
├── datasets/
│   ├── mvtec.py           # MVTec dataset loader
│   └── preprocessing.py   # Data preprocessing script
├── imgs/                  # Sample images for reference
├── results/               # the output images 
├── train_patches/         # MVTec dataset 600000 images 
│   ├── 2.png
│   ├── 3.png
│   └── pic1.jpg
├── models/
│   ├── VAE.py             # VAE model definition
│   └── __init__.py
├── func.py                # Helper functions
├── test.py                # Testing script
├── train.py               # Training script
└── utils.py               # Utility functions
```

## Datasets

The `datasets` directory contains scripts for loading and preprocessing datasets. The primary dataset used is the MVTec Anomaly Detection dataset. Download the dataset from the official website and place it in the appropriate directory `train_patches` folder.

## Results

The results of anomaly detection and localization will be saved in the `results` directory. This includes:

- Original test images
- Reconstructed images
- Pixel-wise anomaly score maps
- Thresholded anomaly localization maps
- ROC curves and AUC scores for anomaly detection performance

These outputs allow for both quantitative evaluation of the model's performance and qualitative assessment of its anomaly localization capabilities.

## Contributing

We welcome contributions! Please open an issue or submit a pull request for any improvements or bug fixes.

## License

