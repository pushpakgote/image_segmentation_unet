# Image Segmentation With U-Net
Built U-Net architecture for image segementation to predict a label for every single pixel in an image.

Semantic image segmentation allows you to predict a precise mask for each object in the image by labeling each pixel in the image with its corresponding class. The word “semantic” here refers to what's being shown, so for example the “Car” class is indicated below by the dark blue mask, and "Person" is indicated with a red mask:

<img src="images/carseg.png" style="width:500px;height:250;">
<caption><center> <u><b>Figure</u></b>: Example of a segmented image <br> </center></caption>

As you might imagine, region-specific labeling is a pretty crucial consideration for self-driving cars, which require a pixel-perfect understanding of their environment so they can change lanes and avoid other cars, or any number of traffic obstacles that can put peoples' lives in danger. 


## U-Net architecture 
<img src="images/unet.png" style="width:700px;height:400;">
<caption><center> <u><b> Figure </u></b>: U-Net Architecture<br> </center></caption>

It consists of Encoder and Decoder :

<div>
<img src="images/encoder.png" style="width:500px;height:500;">
<img src="images/decoder.png" style="width:500px;height:500;">
</div>

The Encoder decreases height and width of input image while increasing no. of filters and Decoder upsamples height and width while decreasing no. of filters and cancatenating skip connections from Encoder.

The dataset can be downloaded from kaggle: https://www.kaggle.com/datasets/kumaresanmanickavelu/lyft-udacity-challenge?select=dataA
