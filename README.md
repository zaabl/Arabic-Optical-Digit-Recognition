# Arabic-Optical-Digit-Recognition
In this repository a handwritten Arabic digits OCR is implemented using TensorFlow Keras.

## Overview
This notebook builds an OCR for handwritten Arabic digits, research in OCR or optical character recognition started a long time ago in order to allow the computer to understand the words in any visual image, but the peak in OCR performances did happen in the deep learning era as it introduced advanced methods and techniques in order to achieve the OCR's outstanding outcomes and uses. The dataset used will be MADbase from the electronics engineering department, in the American University in Cairo, and the CNN will be build using Keras from TensorFlow.

## Dataset
The dataset is composed of 70,000 digits written by 700 participants. Each participant wrote each digit (from 0 to 9) twenty times (ten times only used in our database – the other ten times may be used later in writer verification research). To ensure including different writing styles, the database was gathered from different institutions: Colleges of Engineering and Law, School of Medicine, the Open University (whose students span a wide range of ages), a high school, and a governmental institution. Forms were scanned with 300 dpi resolution then digits are automatically extracted, categorized, and bounded by bounding boxes. We adjusted the scanner to produce binary images directly; so we did not need to binarize the resulting images. Some noisy and corrupted digit images were edited manually. The database is partitioned into two sets: a training set (60,000 digits – 6000 images per class) and a test set (10,000 digits – 1000 images per class). Writers of training set and test set are exclusive. Ordering of including writers to test sets are randomized to make sure that writers of test set are not from a single institution (to ensure variability of the test set).

http://datacenter.aucegypt.edu/shazeem/

## Model's Architecture
We will use keras for the creation of our model, we will start by creating a function for use to create our model, we will set the activation, optimizer and our initializing method as variables for us to easly modifiy it in the hyper-parameter tuning phase.We will start by creating our first convolutional layer and setting up the input shape, we will create additional pooling layer along with a batch normalization layer, then we will add three convolutional layers with the same structure but the the double size of filters each layer.Then we will flatten our layer preparing it for the fully connected layers, we will use a small neurons numbered layer with a drop out layer, batch normalization and we will add an L2 regularizer so we will control the overfitting.


![architecture, digits](https://user-images.githubusercontent.com/32912214/134216269-bc65ad99-949d-4b33-952e-4f9d45672c6a.png)

## Acknowledgments

• Author: **Hossam Zaabl**

https://github.com/zaabl

• Sherif Abdelazeem, Ezzat El-Sherif, Electronics Engineering Dept., The American University in Cairo

http://datacenter.aucegypt.edu/shazeem/

• Amr Hendy, Arabic Handwritten Image Recognition

https://github.com/AmrHendy/Arabic-Handwritten-Images-Recognition
