#Data

##Python

X.npy and Y.npy are numpy array that can be loaded using the "numpy.load" function.
X corresponds to a (2062,64,64) array of float numbers, between 0 and 1. This 
corresponds to 2062 grayscale images of 64x64 pixels each.
For example:
X[55] returns the matrix of (64,64) pixels for the 55th image.
X[42][4][7] is the pixel value for coordinates (4,7), of image 42. 
Y is a (2062,10) array of integers from which the label can be deduced. For example,
Y[55] is the label for X[55].
Labels are one-hot encoded. There are 10 labels. 
0 is encoded as [1,0,0,0,0,0,0,0,0,0]
1 is encoded as [0,1,0,0,0,0,0,0,0,0]
2 is encoded as [0,0,1,0,0,0,0,0,0,0]
etc.
However, the label value and the sign language value do not correspond. Mapping is
given in the "classLabels.txt" file. For example,
Y[55] = [1,0,0,0,0,0,0,0,0,0]
This corresponds to a label of 0, which corresponds to the sign language for 9.

##Matlab (or other)

The "matlab" folder contains the 2062 .png images. Each file has name of format:
img_i_k.png
...where i is the image number and k is the image label (here, the label corresponds 
to the sign language value). For example,
img_0055_9.png is the 55th image and it corresponds to a 9 in sign language.



