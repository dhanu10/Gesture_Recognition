# Project Name

Predicting Gestures from video frames using CNN , LSTM Networks

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information

Analysis of Video frames :

This repository contains an analysis of the Video clips from the Gesture Recognition dataset. The dataset contains more than 600 training videos and 100+ validation videos, each video containing 30 image frames, with the goal of building models to detect gestures - left, right, up, down , none which can be used in smart TV.
Objective is to enhance learning of CNN 2D , 3D and LSTM/GRU.

Problem Statement:
To build a CNN 2D, 3D based model in addition to combination of  LSTM/GRU layers which can accurately detect Gesture.

Dataset:

The dataset consists of over 600+ training videos and 100+ validation videos to train and test the models using different approaches.
The dataset was converted into numpy arrays using PILLOW python model, resized to 64 X 64 or 128 X 128 and normalised by /255 factor.

Modelling and Data Strategies:

Data adjustments - Number of samples i.e. frames from each video were changed. Every alternate frame was chosen. In most of the cases, 90%+ frames were used.
Image size was cropped down to 64 X 64 for all models except transfer learning which accepts 128 X 128 or 256 X 256 size. Downscaling was preferred over upscaling of images.
Batch sizes of 16 and 32 were attempted. Also randomness was applied in building batches in the training and it was avoided in validataion batches.
Generator object was created to handle training and validation in batches.

Several modelling strategies were used. First CNN 3D models were built. LSTM/GRU layers were added to CNN 3D models to confirm impact on accuracy. 
These layers allwoed model to consider temporal dependency within the sequences.
CNN 2D models including LSTM/GRU layers and finally transfer learning using mobile net network was also used to train the model.


This assignment helps reenforce some of the concepts about image processing, CNN modeling, LSTM/GRU Layers.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
In this analysis, we used various model techniques, particularly generator to execute training and validation in batches.
3D CNN appears to have provided consistent , better results wiht accuracy reaching upto 50% with roughly 50 epochs.
Similarly approach of transfer leanring using standard *NET models feeding to GRU yielded more than 70% accuracy on validation dataset. If model is trained further for another 50 epochs, we may  get better results.
Availability of GPU power is major limitation in the exercise.
While Dropout layer appears important, validation loss and accuracy didn't improve much with BatchNormalisation or by preparing very complex models.
One of the complex models with large number of parameters was ineffective in learning.


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Python : 3.8
- Pandas Version : 1.5.0
- Numpy  Version : 1.23.4
- Seaborn Version : 0.12.0
- Matplotlib Version : 3.6.2
- Tensorflow / keras : 

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Use of this dataset in publications is from following publication:
International Skin Imaging Collaboration (ISIC) dataset



=========================================
Contact
=========================================
	
For further information about this dataset please contact - Upgrad


## Contact
Created by [@dhanu10] - feel free to contact me or [@shajivmasters] !


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
