# Blurry-Car-License-Detection

This project's purpose is to detect if a car license is Blurry from the desired image. The input dataset contains unstructured and noisy data. To deal with such a dataset various methods of image preprocessing are applied.

Some samples of dataset images: 

![alt text](https://github.com/mahsaghn/Blurry-Car-License-Detection/blob/main/sample1.png)
![alt text](https://github.com/mahsaghn/Blurry-Car-License-Detection/blob/main/sample2.png)

## Data Augmentation
Due to the nature of the dataset, zoom in, zoom out, rotating with an angle in a specific range and adjusting the brightness of images generate new images that are all possible and valid data. 

![alt text](https://github.com/mahsaghn/Blurry-Car-License-Detection/blob/main/augmentation.png)

## pre-processing
Each of the following methods are implemented. Each has some advantages and disadvantages.
- CLAHE
- Sobel Edge detector
- Morphology Operators to detect license area

For a powerful neural network such as ResNet it is possible to classify this task without such preprocessing.

## Model Architecture
Contains Clear Car license pre-trained ResNet Neural Network is used at the top of the model in order to extract features from input processed images; then, 2 dense layers classifies the images into three desired categories: 
- Do not contain any car license
- Contains Car license if blurry
- Contains Clear Car license
