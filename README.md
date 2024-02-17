# Pneumonia Detection Project


## Overview

This project focuses on the detection of pneumonia using chest X-ray images. It employs a Convolutional Neural Network (CNN) built with TensorFlow and Keras to classify X-ray images into normal and pneumonia cases.

## Dataset

The dataset used for training and evaluation is available on Kaggle: [Chest X-ray Pneumonia Dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia).

## Getting Started

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/pneumonia-detection.git
   cd pneumonia-detection
   ```

2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download the Dataset:**
   - Obtain the Kaggle API key and place it in the root directory as `kaggle.json`.
   - Run the following commands:
     ```bash
     kaggle datasets download -d paultimothymooney/chest-xray-pneumonia
     unzip -qq chest-xray-pneumonia.zip
     ```

4. **Train the Model:**
   - Execute the notebook or run the provided Python script for training the model.

## Model Architecture

The CNN model architecture used for pneumonia detection:

```plaintext
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #
=================================================================
conv2d (Conv2D)              (None, 254, 254, 32)      896
_________________________________________________________________
batch_normalization (BatchNo  (None, 254, 254, 32)      128
_________________________________________________________________
max_pooling2d (MaxPooling2D)  (None, 127, 127, 32)      0
_________________________________________________________________
...
dense (Dense)                (None, 1)                 129
=================================================================
Total params: xxx,xxx
Trainable params: xxx,xxx
Non-trainable params: 0
```

## Data Augmentation

The training dataset is augmented using various transformations such as rotation, shift, shear, zoom, and more to enhance model generalization.

## Training and Evaluation

The model is trained for 10 epochs with the Adam optimizer and binary crossentropy loss. The training and validation accuracy are monitored.

```bash
python train.py
```

## Prediction

Predictions can be made on new images using the trained model. Example:


## Results


## License

This project is licensed under the [MIT License](LICENSE).

