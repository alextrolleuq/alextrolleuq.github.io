# An Exercise in Transfer Learning

Table of contents:

1. TOC
{:toc}

## The Assignment

Our assignment wanted us to create a jupyter notebook to classify the same classes as the CIFAR10 dataset. These are the following classes:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

To do this, I followed and copied most of the code we were handed out. It had to scrape images of the net with Duck Duck Go, and it went great with all the classes, except the dog class.
I suspect the photo of a dog that it tried to import was copyrighted or something like that. I believe it was restricted, so the code fail in showing it. I could get the url and have 
a look at it manually, but I wanted the machine to be able to do it aswell. I ended up changing the search bar into 'small dog images' instead of 'dog photos', then it worked nicely.
This was ofcourse only when I wanted to see if the classes worked. When I retrieved many example images (200 of each class), then I used 'dog photo', as I also removed teh instances that didn't load correctly so the code wouldn't fail.

I didn't really have any other hickups. I used ResNet18 as it is an easy and relativley shallow (18 layers is deep, but nothing compared to the huge advanced CNNs), but
if I do it again in some point in time I think it would be a good idea to use a CNN thats already been trained on the CIFAR10 classes. I believe this to be possible ass CIFAR10 is well known.

## Confusion Matrix
Here is my confusion matrix:

![Confusion Matrix]("C:\Users\aaale\Downloads\438223487_1472977886927574_3038152678348461733_n.png")

As we can see, it worked pretty good, with the only major problems being that automobile and truck misclassified each other quite a bit. It does make sense though, as I personally would classify them both as 'cars'.
