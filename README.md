# Dataset_multiplier_for_yolo5
The simple scirpt that mulitplies items in the dataset by simple geometrical operations


The scripts were made during a projectof detecting very small objects on large images. The images We worked with were of the size of 10kx10k pixels with several tens of objects on them, of the size of 10x10 pixels. 

The limited amount of images and the limited amount of objects on the forced us to pursue a method to increase the size of the dataset. Processing such large images turned out to be also over the capabilities of the PC that was t oour disposal

The scripts divide images into equally sized, smaller imgs and applies operations of rotation and mirroring to generate 8 (including the original) distinct images for each cut. Then also the label list files are created to match rotated images 

Then there are scripts to adjust the final dataset, which should contain abt 10% of "empty images", as advised by the yolov5 creators.

The script that utilizes yolov5 image detecion models divides each picture from the test set into a set of images with the same resolution as the imgs used in the training set. Then at the end, it stiches the images together to present final results on the unchanged image
