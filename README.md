# covid19Dataset
This repository contains the dataset for Unitn Algoritmi Avanzati 2020 project. The code is in this [Google Colab Notebook](https://colab.research.google.com/drive/1tTcINLbBPCb3XQDNEGBkENXJpaOUBbLE?usp=sharing).

## Report
The file report.pdf contains the report of the project.

## Dataset
**Data**: we have ~6000 thoracic x-ray images, each one has a 256x256 pixels resolution. These images have been obtained on people affected by one of the three illnesses or people without any illness. As usually done when developing such an algorithm, we need to make some considerations:
 
1. **Subdivision of the data into splits**: as said before, we have ~6000 images at our disposal. Despite this fact, we cannot use them all just to develop our algorithm, but we need to reserve a part of them in order to test the algorithm performances. For this reason, we will divide the ~6000 images into three splits: train, validation and test. The train and validation splits will be given with their corresponding ground truth, meaning that for each thoracic x-ray image we will also know its label. On the other hand, for the test split, only the images will be given. The train and validation splits will be the two splits that you can use to develop and improve the algorithm, while the test split will be used in order to verify the performances of the algorithm on data on which the algorithm has not been trained on and has never seen before. 

    This table shows statistics about the three splits.


    Split / Class | Normal | Bacterial | Viral | COVID-19 | Total
    --------------|--------|-----------|-------|----------|------
    train | 951 | 1664 | 909 | 45 | 3569 | 
    validation | 313 | 553 | 303 | 20 | 1189 
    test |319 | 569 | 292 | 11 | 1191 
    total | 1583 | 2786 | 1504 | 76 | 5949 
    
    Given the ~6000 images, we consider ~60% for train, ~20% for validation and the remaining ~20% for test. 

2. **Number of images for each class**: as you can see from the table above, the number of images for each class is fairly different. In particular, the number of COVID-19 images is very limited. This is a very common issue which is usually found in many datasets, also known as class imbalance. In order to obtain the best results, it will be very important to take this class imbalance into account.

3. **Additional data**: in order not to limit the choice of the algorithm to use, we will provide you with some additional data. On top of the images, we will also provide a set of features which have been extracted and will be potentially meaningful in order to solve the task. 

## Plots
Plots folder contains plots about the results of training/evaluating the classifiers I used.

## Log.txt
log.txt file contains logs about the training/evaluation of the classifiers I used.
