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

## Features

- Variational Auto Encoder with feature augmentations
- Anomaly detection and localization
- Support for MVTec Anomaly Detection dataset
- Easy to use training and testing scripts

## Installation

Clone this repository and install the required dependencies:

```bash
git clone https://github.com/Kidus-Bellete/FAVAE_Anomaly_Detection_And_Localization.git
cd FAVAE_Anomaly_Detection_And_Localization
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
│   ├── 4.png
│   ├── 5.png
│   ├── 6.png
│   ├── 7.png
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

The `datasets` directory contains scripts for loading and preprocessing datasets. The primary dataset used is the MVTec Anomaly Detection dataset. Download the dataset from the official website and place it in the appropriate directory.

## Results

The results of anomaly detection and localization will be saved in the `results` directory. This includes images with localized anomalies highlighted.

## Contributing

We welcome contributions! Please open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
