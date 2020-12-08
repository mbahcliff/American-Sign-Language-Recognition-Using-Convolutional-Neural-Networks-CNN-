# American-Sign-Language-Recognition-Using-Convolutional-Neural-Networks-CNN-
# Abstract
This project has to do with applying Covolutional Neural aNetworks to American Sign Language(ASL). In deep learning, a convolutional neural network (CNN, or ConvNet) is a class of deep neural networks, most commonly applied to analyzing visual imagery. It has been one of the most influential in the field innovation in the field of computer vision. 
# Introduction
American Sign Language (ASL) is a complete, natural language that has the same linguistic properties as spoken languages, with grammar that differs from English. ASL is expressed by movements of the hands and face. It is the primary language of many North Americans who are deaf and hard of hearing, and is used by many hearing people as well.
he dataset format is patterned to match closely with the classic MNIST. Each training and test case represents a label (0-25) as a one-to-one map for each alphabetic letter A-Z (and no cases for 9=J or 25=Z because of gesture motions). The training data (27,455 cases) and test data (7172 cases) are approximately half the size of the standard MNIST but otherwise similar with a header row of label, pixel1,pixel2….pixel784 which represent a single 28x28 pixel image with grayscale values between 0-255.

![amer_sign2](https://user-images.githubusercontent.com/63025220/101502360-db9a2500-393e-11eb-99ad-582cd0d25cd5.png)

# Problem statement
Communication is an important part of our lives. Deaf and dumb people being unable to speak and listen, experience a lot of problems while communicating with normal people. There are many ways by which people with these disabilities try to communicate. One of the most prominent ways is the use of sign language, i.e. hand gestures. It is usaully develop for normal people to understand this sign language without an interpreter. That's why it is necessary to develop an application for recognizing gestures and actions of sign language so that deaf and dumb people can communicate easily with even those who don’t understand sign language. The objective of this work is to take a step in breaking the barrier in communication between the normal people and deaf and dumb people with the help of sign language.
# Business goal
The business goal is to develop an application which is able to recognize gestures and actions of sign langauges and interprets them to normal people. This way normal people can effectively communicate with people who are deaf and dumb without any need to go to a sign lsanguage school
# Data source
Data is publicly available on ksaggle and you can find it also in my respiratory
# Looking at the first five rows of my train and test data respectively
## Train data

![Capture51](https://user-images.githubusercontent.com/63025220/101510080-75fe6680-3947-11eb-97b4-c6ae9e81cf28.PNG)

## Test data

![Capture52](https://user-images.githubusercontent.com/63025220/101510305-c249a680-3947-11eb-9b81-2f3e0eef3ade.PNG)

# Data Augmentation
It is a technique used to to artificially expand the the size of a training dataset by creating modified version of image in the dataset. 
In order to avoid overfitting problem, we need to expand artificially our dataset. We can make your existing dataset even larger. The idea is to alter the training data with small transformations to reproduce the variations.

# Data Visualization
## Label count

![Capture53](https://user-images.githubusercontent.com/63025220/101513135-d393b280-3949-11eb-8614-1cd7e3be306a.PNG)
## Preview of images in the train data set

![Capture54](https://user-images.githubusercontent.com/63025220/101513392-1c4b6b80-394a-11eb-991b-b95ce2ca7504.PNG)


# Bulind my CNN model
The model consist of :

Three convolution layer each followed bt MaxPooling for better feature capture
A dense layer of 512 units
The output layer with 24 units for 24 different classes
## Convolution layers

Conv layer 1 -- UNITS - 128 KERNEL SIZE - 5 * 5 STRIDE LENGTH - 1 ACTIVATION - ReLu

Conv layer 2 -- UNITS - 64 KERNEL SIZE - 3 * 3 STRIDE LENGTH - 1 ACTIVATION - ReLu

Conv layer 3 -- UNITS - 32 KERNEL SIZE - 2 * 2 STRIDE LENGTH - 1 ACTIVATION - ReLu

MaxPool layer 1 -- MAX POOL WINDOW - 3 * 3 STRIDE - 2

MaxPool layer 2 -- MAX POOL WINDOW - 2 * 2 STRIDE - 2

MaxPool layer 3 -- MAX POOL WINDOW - 2 * 2 STRIDE - 2

## Dense and output layers

![Capture55](https://user-images.githubusercontent.com/63025220/101522431-350d4e80-3955-11eb-97e8-d6f19f295928.PNG)

## Training the model

### The model trains for eporchs = 35

![Capture56](https://user-images.githubusercontent.com/63025220/101522691-933a3180-3955-11eb-8fcc-44af34f072a8.PNG)

# Model evaluation on test set

![Capture58](https://user-images.githubusercontent.com/63025220/101523120-28d5c100-3956-11eb-8190-a32d124efe11.PNG)

# Plots of the accuracy and loss between trainig and validation data

![Capture59](https://user-images.githubusercontent.com/63025220/101523572-c7fab880-3956-11eb-92f4-0885b6a4cd30.PNG)

# Classification report

It helps usin identifying the misclassified classes in more details

![Capture70](https://user-images.githubusercontent.com/63025220/101524006-6129cf00-3957-11eb-9c37-1746d0eb48bf.PNG)

# Confusion matrix

![Capture71](https://user-images.githubusercontent.com/63025220/101524194-a0582000-3957-11eb-9563-3c8e6b0e5b36.PNG)

# Predicting labels
## correct labels

![Capture72](https://user-images.githubusercontent.com/63025220/101524445-eca36000-3957-11eb-9323-c79845a5dd88.PNG)




