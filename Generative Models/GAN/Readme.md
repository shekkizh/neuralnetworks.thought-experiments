...Still under edit


##Difficulties training a Generative Adversarial Networks 
So GANs are like the happening thing in Deep learning right now (I mean even Yann Lecun said so right!). But this writeup is not about how awesome GANs are (which they are :punch:), 
this is going to be more on how freaking difficult it is to train these models. I believe GANs might be slightly ill posed as a problem for training with gradient descent. 
Took me quite some time to figure out why the hell my model was not working at all - hoping to throw some light for those folks who might fall in the same pit while trying to implement GANs. 

For a basic introduction to generative models and GANs refer to my notes [here](https://github.com/shekkizh/neuralnetworks.thought-experiments/blob/master/Generative%20Models/README.md). 

1. [Introduction](#introduction)
2. [Observations](#observations)
3. [Results](#results)
4. [References and Useful links)(#references-and-useful-links)

##Introduction

##Observations
![](logs/discriminatorLoss.png)   ![](logs/discriminatorRealLoss.png)   ![](discriminatorFakeLoss.png)

![](logs/GeneratorLoss.png)

![](logs/DiscriminatorPred.png)   ![](logs/GeneratorPred.png)

![](logs/DiscriminatorFirstLayer.png)   ![](logs/GeneratorFirstLayer.png)

**Failed Training Observations** 

![](logs/DiscriminatorFirstLayerFailed.png)   ![](logs/GeneratorFirstLayerFailed.png)

![](DiscriminatorPredFailed.png)

##Results
CelebA

![](images/GAN_Faces/epoch1_sample1.png)![](images/GAN_Faces/epoch1_sample2.png)![](images/GAN_Faces/epoch1_sample3.png)
![](images/GAN_Faces/epoch2_sample1.png)![](images/GAN_Faces/epoch2_sample2.png)![](images/GAN_Faces/epoch2_sample3.png)
![](images/GAN_Faces/epoch3_sample1.png)![](images/GAN_Faces/epoch3_sample2.png)![](images/GAN_Faces/epoch3_sample3.png)
![](images/GAN_Faces/epoch6_sample1.png)![](images/GAN_Faces/epoch6_sample2.png)![](images/GAN_Faces/epoch6_sample3.png)
![](images/GAN_Faces/epoch8_sample1.png)![](images/GAN_Faces/epoch8_sample2.png)![](images/GAN_Faces/epoch8_sample3.png)
![](images/GAN_Faces/epoch10_sample1.png)![](images/GAN_Faces/epoch10_sample2.png)![](images/GAN_Faces/epoch10_sample3.png)
![](images/GAN_Faces/epoch12_sample1.png)![](images/GAN_Faces/epoch12_sample2.png)![](images/GAN_Faces/epoch12_sample3.png)
![](images/GAN_Faces/epoch15_sample1.png)![](images/GAN_Faces/epoch15_sample2.png)![](images/GAN_Faces/epoch15_sample3.png)

Flowers

![](images/GAN_Flowers/sample1.png)![](images/GAN_Flowers/sample2.png)![](images/GAN_Flowers/sample3.png)
![](images/GAN_Flowers/sample4.png)![](images/GAN_Flowers/sample5.png)![](images/GAN_Flowers/sample6.png)
![](images/GAN_Flowers/sample7.png)![](images/GAN_Flowers/sample8.png)![](images/GAN_Flowers/sample9.png)
![](images/GAN_Flowers/sample10.png)![](images/GAN_Flowers/sample11.png)![](images/GAN_Flowers/sample12.png)
![](images/GAN_Flowers/sample13.png)![](images/GAN_Flowers/sample14.png)![](images/GAN_Flowers/sample15.png)
![](images/GAN_Flowers/sample16.png)![](images/GAN_Flowers/sample17.png)![](images/GAN_Flowers/sample18.png)
![](images/GAN_Flowers/sample19.png)![](images/GAN_Flowers/sample20.png)![](images/GAN_Flowers/sample21.png)
![](images/GAN_Flowers/sample22.png)![](images/GAN_Flowers/sample23.png)

##References and Useful links
