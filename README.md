# TensorFlow_Image_Classification
Image classification using tensor flow library.

Image CLassification can be done by making use of a Pre-trained CNN model called Inception , which was trained by Goolge on around 100k images.

In this project I've worked on this model to classify the images into 3 types: the popular characters from the DragonBall  
franchise : Goku , Vegeta and Trunks.

## Prerequisites:

1) Tensor flow library can be insatlled on your machine from the souce: https://www.tensorflow.org/install/

2) Follow my Goolge drive link to download the required files:     https://drive.google.com/drive/folders/14aA1C6LsuoegiEZ4xhRjHJU10A1Xx9TZ?usp=sharing

## Classifying the image:

1) Extract the .zip file downloaded from my Google drive link.

2) Open the terminal in that folder.

3) We are gonna classify this image now:

![vegito3](https://user-images.githubusercontent.com/37662337/40265513-50699d3e-5b57-11e8-92b9-872a6980b631.jpg)

As one of these 3:

![gvt1](https://user-images.githubusercontent.com/37662337/40265531-ae332cc8-5b57-11e8-9d08-f999c504e171.png)

A gentle reminder that we have trained the classifier on Goku , Vegeta and Trunks pics individually i.e we have not trained their fusion images like (Gogeta, Vegito)

We have to type in the following command on the terminal:

python -m scripts.label_image   --graph=tf_files/retrained_graph.pb    --image=tf_files/dbz/vegito3.jpg

Here:
     --graph=tf_files/retrained_graph.pb is the code to predict the label of the input image.
     
     --image=tf_files/dbz/vegito3.jpg is the input image 
     
 and the obtained output is:
 
 
     


