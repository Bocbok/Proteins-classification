# Human protein classification

# V1

In the first version of my project I downloaded all the images on my computer, then loaded it all in numpy arrays that I saved so I can load them faster.
My idea was to "superpose" the 4 images in one 4 dimension image.
To do this I rescaled all the images and put them in grayscale.
Then I created an array of these images of dimension (256, 256, 4) to do my training.

Due to various problems of "out of memory" I couldn't go until the end of the training and then do the submission.

# V2

For the second version I used a [kaggle notebook ](https://www.kaggle.com/rejpalcz/cnn-128x128x4-keras-from-scratch-lb-0-328) that use the same technique as I do eg superpose the 4 images in one.
The images are loaded via a DataGenerator so it prevents the out of memory errors I had with my large numpy arrays.

## Model used

* Image size : 192 x 192
* Batch size : 64
* Epochs : 40

![](https://i.imgur.com/uwiQGvc.png)

![](https://i.imgur.com/vPpJPoU.png)

On my validation set I have a Macro F1-score CV of 0.2758 which leads to 0.13417 of scoring on kaggle.
