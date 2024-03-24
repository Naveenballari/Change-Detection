# Change Detection on Hyper-spectral Imagery
## Problem Statement
Semantic segmentation change detection with U-net architecture on hyper-spectral imagery.

## Introduction
### Change Detection: 
Identifying differences in the  object or phenomenon by observing at different times. Automatic change detection takes sequential images of the same location as inputs and produces a binary map which marks the changes.Change detection technology makes it easier and faster to observe the world. 

### Remote Sensing Images: 
The process of detecting and monitoring the physical characteristics of an area by measuring its reflected and emitted radiation at a distance. These are widely used in change detection process such as disaster assessment, urban planning, environment pollution monitoring  etc.

## Objectives 
1. To apply pre-process dataset preserving the ROI of hyperspectral images.<br>
2. To apply semantic segmentation technique to label each pixel in the hyperspectral images.<br>
3. To detect meaningful and accurate locations of change in  information from hyperspectral images.<br>
4. To extract information with least error possible and finally conclude changes occurred in hyperspectral images.<br>

## Dataset details
Dataset is collected from Indian Pine Site 3 AVIRIS hyperspectral dataset
Dataset consists of 145x145 pixels and 224 spectral reflectance bands in the wavelength range 0.4–2.5 10^(-6) meters.
The Indian Pines scene contains two-thirds agriculture, and one-third forest or other natural perennial vegetation. 
Dataset includes ground photos of several fields in mat format. 

## Architecture Design
### Standard U-Net Architecture
standard U-Net architecture is designed based in the Convolutional Neural Network.
It consists of expanding and contracting path.
The contracting path consists of many convolutional layers and a max pooling layer.
the expanding path consists of upsampling blocks followed by convolutional blocks.
standard U-Net architecture can be modified using by changing the number of layers to improve performance
### Attention U-net architecture
Attention U-Net improves U-Net by incorporating attention mechanism which allows model to focus more on important features.
The Attention U-Net adds attention gates to the skip connections, which allow the model to selectively weigh the importance of the features being passed from the encoder to the decoder. The attention mechanism in Attention U-Net is added to the skip connections between the encoder and decoder networks. 

## Results
Four evaluation metrics were chosen to evaluate the performance of the used
Architectures namely, Precision, Recall, F1-score and Kappa Coefficient.<br>
Precision is the ratio of the average number of successfully identified images
to the total of number of correctly and incorrectly identified images using the
reference input.<br>
Recall is defined as the average proportion of correctly identified images among
all correctly and incorrectly identified images.<br>
F1 score is defined as if the obtained value reaches 1, it is considered as best,
and if it reaches 0, as worst.<br>
Kappa coefficient is used an index to express the accuracy of an image classification used to produce a thematic map.<br>
Results are shown in below table.
<br>
|Model|Precision|Recall|F1_score|Kappa|
|-----|---------|------|--------|-----|
|Standard U-net|0.847|0.987|0.911|0.902|
|Attention U-net|0.885|0.974|0.927|0.920|
<br>
With the above performance metrics with different models we can infer that
Attention U-Net performs best for change detection mechanism.
