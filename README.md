# Image Captioning

## About Project

Image Captioning is the process of generating textual description of an image. It uses both Natural Language Processing and Computer Vision to generate the captions. In the past few years, the problem of generating descriptive sentences automatically for images has garnered a rising interest in natural language processing and computer vision research. Image captioning is a fundamental task which requires semantic understanding of images and the ability of generating description sentences with proper and correct structure.

In this project, we have proposed a hybrid system employing the use of multilayer Convolutional Neural Network (CNN) to generate vocabulary describing the images and a Long Short Term Memory (LSTM) to accurately structure meaningful sentences using the generated keywords. The convolutional neural network compares the target image to a large dataset of training images, then generates an accurate description using the trained captions of the Flickr8k Dataset.

## About Dataset

Flicker8K Dataset: 
It Consists of 8092 Images in jpeg format with different shapes and sizes. It’s a small dataset, but it contains a variety of images. The images were chosen from six different Flickr groups, and tend not to contain any well-known people or locations, but were manually selected to depict a variety of scenes and situations. Each Image Consists of a set of 5 captions. Each caption describes the activity in the given images with different sentence structure. Images are paired with five different captions which provide clear descriptions of the salient entities and events. This small dataset was chosen in order to train a model quickly. Dataset Contained a text file with 1 line for each caption.There were 40460 lines i.e 5 * 8092 lines in that text file. Also, 8092 images were inside a folder. 

**The directory structure was like :-**
> Flicker8K_Dataset: A folder which contain 8092 Images in jpeg format
> 
> Flickr8k.token.txt: A text file with 40460 lines i.e  5 captions for each image out of 8092 total images  

## About Architecture

**Pseudo Architecture**


> ![image](https://user-images.githubusercontent.com/63506466/137242734-3565f80f-2b7c-4d2d-b1ac-ecc577fa32f8.png)


**Actual Architecture** 

The architecture of the chosen model is shown in the above figure 4.4. Model architecture is in Shape of the English letter ‘Y’. One hand of ‘Y’ served as an Image Input, where 2048 dimensional precomputed image encodings were provided. Whereas, the other hand of ‘Y’ served as Caption Input, where tokenized captions were passed to Embedding Layer. These embeddings were taken from pretrained Glove Embeddings, in which each word is represented by a 50 dimensional vector based on its relation with other words in corpus. The tail of ‘Y’ predicts the next word in the partial caption

> ![image](https://user-images.githubusercontent.com/63506466/137241694-7ad652b5-ccea-4e97-beca-80b902dad5ea.png)


## Example Prediction

**Image**

> ![image](https://user-images.githubusercontent.com/63506466/137243187-0b6a43c7-6e20-41f3-9c59-9e0c98852a45.png)


**Caption**

> a girl in a crowd its red hair with up a yellow girl in a yellow dress endseq

## Colab 

https://colab.research.google.com/drive/16C6PEUYUA9fa8HARz3IK-i3RmsuMxTrG?usp=sharing#scrollTo=T9-xn-aaXgjT

