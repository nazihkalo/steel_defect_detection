# Detecting Defects in Steel Manufacturing Line using Computer Vision

## This is my attempt at the Severstal Kaggle competition for deteSeverstal

Here is a description of the competition/objective:
-----
==> **In this competition, you’ll help engineers improve the algorithm by localizing and classifying surface defects on a steel sheet.**

I will be using images from high frequency cameras to power a defect detection algorithm.


## Here are samples of the different kinds of defects (each combination from the training set is represented here)

![2](images/image2.png)
![2](images/image3.png)
![2](images/image4.png)
![2](images/image5.png)
![2](images/image6.png)

## Here is the distribution of different classes within the dataset
![2](images/charts1.png)
![2](images/charts2.png)

## Model Summary

I will be using [segmentation-model](https://github.com/qubvel/segmentation_models#models-and-backbones) package to load pretrained weights.

I will be using the basic Unet architecture with a resnet backbone, which has pre-trained weights for faster and better convergence.
- Note: The resnet backbone here means that resnet model weights will be used as the encoder part (the first half) of the UNet, and from which the decoder part (the second half) will be programmatically built up. The idea is to enable use of a proven image classification architecture with pre-trained weights for transfer learning benefits.
![res2unet](images/resnet2unet.png)

## Predictions
![2](images/predictions.png)
