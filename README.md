# Dog Recognition System

This repository contains a system for recognizing dogs using a combination of object detection and siamese neural network models.

## Overview

- `Dog_Detection`: Contains the YOLOv8 model implementation for real-time dog detection.
- `Dog_Data`: Contains close-up images of 100 different dogs' noses used for training the siamese model.
- `dog_siamese_model.ipynb`: Jupyter Notebook for training and saving the siamese model to recognize whether two dogs are the same or not.
- `prediction.ipynb`: Jupyter Notebook for loading the trained encoder and siamese model weights to perform predictions on dog images.

## Dog Detection

The `Dog_Detection` folder contains the YOLOv8 implementation (`dog_detection.ipynb`) that detects dogs in real-time video streams. It draws bounding boxes around detected dogs for visualization.

![download](https://github.com/maskboyAvi/Dog_Nose_Recognition/assets/123640350/e7d20f6e-388c-4948-a02d-2895ee383c7f)


## Siamese Model

The siamese model (`dog_siamese_model.ipynb`) is trained using the close-up images of dog noses from the `Dog_Data` folder. The trained encoder and siamese model weights are saved in separate folders (`encoder_folder` and `siamese_model_folder`, respectively).

### Encoder Training

The encoder is trained using transfer learning with the Xception architecture on the dog nose images dataset.

![Screenshot (271)](https://github.com/maskboyAvi/Dog_Nose_Recognition/assets/123640350/98a8eb00-2df5-4da8-b068-9f4aefb4b169)

### Siamese Model Training

The siamese model is trained to recognize whether two dogs are the same or different based on their nose images.

![Screenshot (272)](https://github.com/maskboyAvi/Dog_Nose_Recognition/assets/123640350/88b4b5fb-c15e-49c0-b276-50881f09dfd9)

## Prediction

The `prediction.ipynb` notebook loads the trained encoder and siamese model weights to perform predictions on pairs of dog images. It predicts whether the dogs in the images are the same or different.

## Usage

1. Clone the repository:

```bash
git clone https://github.com/maskboyAvi/Dog_Nose_Recognition.git
```

2. Follow the instructions in each notebook (`dog_detection.ipynb`, `dog_siamese_model.ipynb`, `prediction.ipynb`) to run the respective models and perform predictions.

## Requirements

- Python 3.x
- TensorFlow 2.x
- OpenCV
- YOLOv8
- Jupyter Notebook
