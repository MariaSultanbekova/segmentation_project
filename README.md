## Hi! This is a semantic segmentation on pytorch. We will be looking for lips in the image. 
Code https://github.com/MariaSultanbekova/segmentation_project/blob/main/lips_segmentation_code.ipynb

Segmentation is the submission of an image to the input of a neural network and receiving an object mask at the output.
Here we will use the classical model for segmentation - U-net. This model gradually compresses the image, and then decompressing, tries to restore the mask.

![header](https://github.com/MariaSultanbekova/segmentation_project/blob/main/unet_architecture.png)

You can see that we are skipping information from earlier layers, something like skip connections. 
The fact is that we use max pooling to reduce the dimension of the image, and therefore the number of calculations, but at the same time we lose a lot of information from the image and in order to restore it, we skip it at each level.



![header](https://github.com/MariaSultanbekova/segmentation_project/blob/main/image_and_mask.png)

This is how the model works: it predicts the mask, it sort of classifies each pixel, whether it belongs to the background or to an object


----------------------------------------------------------------------------------------------------------------------------------------------------

# Results after training

![header](https://github.com/MariaSultanbekova/segmentation_project/blob/main/lips_predicted_mask.png)
