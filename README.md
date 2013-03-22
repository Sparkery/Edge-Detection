Edge-Detection
==============

Take an image and make another with only significant edges of the previous.

The code takes a .ppm file as an input and outputs the contents of the resulting .ppm file. One will need to print to a file rather than the standard output stream for a picture to be made.

The original file is converted into grayscale as to show intensity changes within the picture. The picture is then smoothed using an appropriate matrix in order to eliminate any stray lines that could be considered edges. Visually, this blurs the image. This is called Gaussian Smoothing. The Sobel operator, which are two more matrices, is then used to find the intensity change on a pixel horizontally, Gx, and vertically, Gy. The sum of the absolute value of both constants is the G value. The G values of every pixel except for borders are normalized to 1. The top 85 percentile are considered edges, and these pixels are marked with black color. Every other pixel is marked with white color.

A .ppm file takes up more space than a regular compressed file because a .ppm file keeps RGB data for every pixel in numbers as opposed to symbols. This can make a normally small file unnecessarily large.
