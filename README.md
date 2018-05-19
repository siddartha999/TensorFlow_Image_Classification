# TensorFlow_Image_Classification
Image classification by making use of TensorFlow library.

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
     
 ###### The obtained output is:
 
 <img width="314" alt="vegito3" src="https://user-images.githubusercontent.com/37662337/40265610-0992c258-5b59-11e8-83a4-d21532867cff.png">

That's pretty cool, Vegito is closer to Vegeta than Goku as classified by the classifier :D 

## Training the Data

1) In the 'tf_files' folder I have extracted multiple images of Goku, Vegeta, Trunks into their respective folders.

2) I have used this extension to download first 100 images when searched in Google: https://chrome.google.com/webstore/detail/fatkun-batch-download-ima/nnjjahlikiabnchcpehcpkdeckfgnohf

3) Now, type the following command in the terminal:

       python -m scripts.retrain   --bottleneck_dir=tf_files/bottlenecks   --how_many_training_steps=1000   -- model_dir=tf_files/models/   --summaries_dir=tf_files/training_summaries/"${ARCHITECTURE}"   --output_graph=tf_files/retrained_graph.pb   --output_labels=tf_files/retrained_labels.txt   --architecture="${ARCHITECTURE}"   --image_dir=tf_files/dbz

4) It took me around 5 minutes to train the model.

5) I have used the following resources to understand the concept behind the scenes:
 
        https://www.youtube.com/watch?v=QfNvhPx5Px8
 
        https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/? utm_campaign=chrome_series_machinelearning_063016&utm_source=gdev&utm_medium=yt-desc#0
 
     


