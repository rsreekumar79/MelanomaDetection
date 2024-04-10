# Build a multiclass classification model using a custom convolutional neural network in TensorFlow
> The aim of the project is to build a multiclass classification model using a custom convolutional neural network in TensorFlow. A data set with the data dictionary with 2239 nos of images for training data and 118 nos images for test data are provided for the analysis. The goal is to To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- General Info: The goal is to to build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis. The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

Actinic keratosis
Basal cell carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented benign keratosis
Seborrheic keratosis
Squamous cell carcinoma
Vascular lesion
 
- Background: Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis. The aim is to detect melanoma from the images given as training data.
- Dataset being used: The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

Actinic keratosis
Basal cell carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented benign keratosis
Seborrheic keratosis
Squamous cell carcinoma
Vascular lesion.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions and observations
- A total of 7 nos models were tried out
- The initial results with the raw set of imbalanced data had greater accuracy for the validation dataset. But there was overfitting observed.
- Then tried various options to bring down overfitting.
- First tried dropouts, there was no overfitting, but the accuracy was not high
- Then tried batch normalization without dropouts, found that batch normalization wont help
- The tried image augmentation with dropouts. 
- There was slight increase in accuracy and less overfitting. Still the accuracy levels were not enough.
- It was observed there was severe class imbalance which could have affected the training and the accuracy
- Then tried the image augmentor library, used to generate additional image for each class. The number of images were capped at 800 for each class. data imbalance is not present now.
- But upon training the model, it was found that there was no improvement in accuracy, the accuracy levels are less than acceptable, but there was no overfitting.
- It was also observed that in the final model utilizing the augmentor generated images for smoothening out the imbalance, augmentation at the beginning of the model is doing more harm than good. The accuracy is better when the first layer is NOT image augmentation.
- The best model was found to be the one with dropouts, 3 layers of CNN, two layers of dense layers, and without image augmentation at the beginning.
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Python version 3.8.10
- pandas version 2.0.3
- numpy version 1.23.5
- seaborn version 0.13.0
- matplotlib version 3.5.3
- tensorflow version 2.13.0
- augmentor version 0.2.12

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- https://pandas.pydata.org/pandas-docs/stable/index.html
- https://numpy.org/doc/
- https://seaborn.pydata.org/
- https://plotly.com/python/plotly-express/
- https://matplotlib.org/
- https://www.tensorflow.org/
- https://pypi.org/project/Augmentor/
- 
## Contact
Created by Sreekumar R (https://github.com/rsreekumar79)


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->