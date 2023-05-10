# EE 5907 CA2

writer Wanry Lin

# Attention! the LDA alogrithm of mine performs weak and there may be something wrong that you'd better write a new one. 

## Introduction
This project is built under the requirements of the file "Face Recognition CA2". There is 7 parts in total. The main goal of the project is to classify the face images.

## Technology
The project is based on the following language and libraries:
1. python 3.10
2. tensorflow 2

## Launch
If you want to run the project, you need to download the data set first.
Once you get the data set, you have to take some photos of yourself as a part of the dataset. Don' t need too many, just 10 pictures. Then build a new folder in PIE named Me.
Most important the project read the images from the folder, so you have to put the PIE folder in the same directory as the ipynb file.
Warning The project is build in MacOS, so the data write and read part may not work in Windows.

## Componet
### Part 0
this part is used to read the images from the folder and store them in json file. I made this to reduce the reading dataset work for the following part.

### Part 1
this part is using PCA to reduce the dimension of the image and visualize the distribution of the data in 2D and 3D.

### Part 2
this part is using PCA to reduce the dimension of the image and then apply KNN to classify. compare the predicted label with the truth to get the confusion matrix and score of the model.

### Part 3
this part is similar to part1 but use LDA replacing PCA

### Part 4
this part is similar to part2 but use LDA replacing PCA

### Part 5
this part using PCA to reduce the dimension of the image then apply SVM to classify. SVM model is from the libSVM

### Part 6
this part build a simple CNN model to classify the image

## Main function
### alldata
read all image data from stroed json file

### dataselect
select a given number of persons' images as the data

### sumran
generate n scalars with a given summary

### Gfeature
generate image feature data into matrix format

### dataset
return training set and testing set with given person number,samples number and the ratio

### pca
PCA algorithm

### LDA
LDA algorithm

### KNN
simple KNN algorithm (K can be 1 or other value)

### fitting
train the model

### confusion_matrix
print confusion matrix of the model

### score
print the accuracy, recall, precision and F1 of the model

### Normalize
normalize the feature before SVM train