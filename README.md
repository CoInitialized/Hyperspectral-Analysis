# Hyperspectral-Analysis

## Introduction
Hyperspectral-Analysis is a project that tackles the problem of Hyperspectral image (HSI) classification. The solution of said group of problems is important due to its real-life application like surface mapping using satellite images. Since hyperspectral imaging results in multiple bands of images, the analysis is significantly harder and less intuitive than that of 3D images and is characterized by a higher volume of images.  

## What hyperspectral means

Hyperspectral imaging, like other spectral imaging, collects and processes information from across the electromagnetic spectrum. The goal of hyperspectral imaging is to obtain the spectrum for each pixel in the image of a scene, with the purpose of finding objects, identifying materials, or detecting processes. There are three general branches of spectral imagers. There are push broom scanners and the related whisk broom scanners (spatial scanning), which read images over time, band sequential scanners (spectral scanning), which acquire images of an area at different wavelengths, and snapshot hyperspectral imaging, which uses a staring array to generate an image in an instant.

![image 1](https://miro.medium.com/max/5318/1*V352SbCwGXrN-MTJF5hAtA.png)

Whereas the human eye sees color of visible light in mostly three bands (long wavelengths - perceived as red, medium wavelengths - perceived as green, and short wavelengths - perceived as blue), spectral imaging divides the spectrum into many more bands. This technique of dividing images into bands can be extended beyond the visible. In hyperspectral imaging, the recorded spectra have fine wavelength resolution and cover a wide range of wavelengths. Hyperspectral imaging measures continuous spectral bands, as opposed to multiband imaging which measures spaced spectral bands.

## Our project

We tried to solve the problem introduced in paper: [Exploring 3-D–2-D CNN Feature
Hierarchy for Hyperspectral Image Classification](https://ieeexplore.ieee.org/document/8736016). Having only one hyperspectral image, we want to achive a system that is able to classify the terrain. As eacg dataset consisted of only one photograph, we decided to create our own dataset from it. We splitted the photo into seperate pixels. To each pixel we've added its surounding pixels - 25x25 window. Thanks to that our neural network can classify the pixel based not only by its value, but also what is around it. 

![image2](https://i.stack.imgur.com/Akjg9.png)

As hyperspectral images have extreamly high dimensionality, we have used PCA to reduce number of "color channels" to 30. Such preprocessed data was shuffled, batched and splitted into train, validation and test sets. For experiment tracking we have used [Neptune](https://neptune.ai/). In the first experiment our Pytorch model achived accuracy score of 0.94 on the test set. 


## ToDo
 - More experiments on different datasets
 - Usable .py executable file that uses neural network on provided photo

## Authors:
 - [Arkadiusz Czerwiński](https://github.com/arkadiusz-czerwinski)
 - [Damian Kucharski](https://github.com/damiankucharski)
 - [Krzysztof Kramarz](https://github.com/Fakser)
