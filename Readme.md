# Overview :

This codebase provides a practical workflow for processing, visualizing, and classifying multispectral images of Chardonnay grapevine leaves to detect yellows diseases and confounding symptoms.


# 1. Dataset

The published multispectral image dataset of Chardonnay grapevine leaves, titled "_Multi-year multispectral image dataset of Chardonnay grapevine leaves with yellows disease and confusing symptoms_", is accessible via the following DOI: https://doi.org/10.57745/LTBIME. Some of the images were evaluated using this code.



_5 Classes categories_
Grapevine yellows (class J), healthy leaves (class T), discoloration (class D), Esca (class E), and leafroll (class S).

_Band used_
Only the red band of the spectral imagery is used; however, blue, green, red-edge, or RGB imagery can also be utilized for testing under ambient lighting conditions.

_Training and test_
The re-annotation retained the categories used exclusively for this test. Images collected in 2021, 2022, and 2023 were randomly divided into training and test sets, with 80% of the images used for training, while this process can be repeated.
 - Test Set 1 (In-year evaluation): Images collected between 2021 and 2023 constitute the remaining 20% ​​of the test set. 
 - Test Set 2 (Cross-year evaluation): All images acquired in 2024 serve as an independent test set to evaluate model generalization across
   different years.

## 2. Notebook Structure
This notebook will follow these procedures.

 - **Parameters setting**
Introduce the path for the bands, setting the parameters for data loading, model training, and evaluation.

 - **Data loading and dataset construction**
Load the selected red-band images, parse the filenames, and construct training and testing sets based on the cross-year experiment setup.

 - **Samples visualization**
Before model training, visualize representative red-band images from these five data categories and verify their labels.

 - **Images processing**
Resize the image and apply the intensity normalization and ImageNet normalization required by ResNet-18.

 - **Model configuration and fine-tuning**
Configure an ImageNet pre-trained ResNet-18 model for a 5-class classification task, and fine-tune the selected layer using red band images.

 - **Model training**
The pre-trained  ResNet-18 model was trained for 20 epochs, and the trained model and training history were saved.

 - **Cross-year evaluation and results visualization**
Evaluate the five-class classification performance on test set 1 and the cross-year test set 2 from 2024.
## Citation
If your research utilizes the aforementioned notebook, please cite the DOI provided above.

## Contact information
If you have any questions or feedback, please feel free to contact the authors Shusong Huang, Université de Reims Champagne-Ardenne or Prof. Valeriu Vrabie valeriu.vrabie@univ-reims.fr or using the authors information provided via DOI.

