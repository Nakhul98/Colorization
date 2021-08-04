# Colorization
The purpose of this learning algorithm is not to guess the original colors of an image back onto a grayscale version of the image. Rather, the algorithm will recreate a possible color scheme for an image that could be used to pass a Turing Test and fool a human observer. Our understanding of the model is that our convolutional neural network will try to guess the underlying features of the grayscale image and then map those features to some color values in an a*b space.
The model does not train in an RGB color space. Instead, our training is done in an L*a*b color space, popularly known as the CIELAB color space, where L is the lightness level of each pixel, and (a, b) both correspond to the 4 colors of human vision. This is done by taking some grayscale image as our input and then guessing some a and b values for that image. In our final prediction, we will convert this a*b prediction from our CNN1 into an RGB image by concatenating the 3 channels (L, a, and b).
NOTE: improvements are still in progress
