# Neural-Network-Image-Recognition-with-Scaled-Conjugate-Gradient-Backpropagation-

This is a code to show the effectiveness of Scaled Conjugate Gradient Backpropogation in an image Recognition Neural Network MATLAB code.

To start, 100 photos were taken of myself wearing Nike Sunglasses, Ray Ban Wayfairs, and No Sunglasses at all. These would be the base images used in training, testing and validation in the network. Images were taken from my laptop camera, and I purposefly chose a simple backdrop to cut down on noise and make the network as accurate as possible. 

To understand how the the Images are worked into the neural network, consider the following. 

An image is composed of a matrix of pixels, where each pixel has a distinct color. Those colors may be easily described as a combination of RGB (red green blue) values that make up that specific color. 

This is an full resolution image used of myself wearing no glasses
![None_Fullres_Color](https://user-images.githubusercontent.com/50057221/58292982-9e3c6980-7d91-11e9-96af-3c0873583c5e.jpg)

This is a collage example of a small sample of images being used for the network, including myself wearing Nike, Ray Bans, and no Sunglasses as well as a collection of different angles of looking. In total there are 100 of each scenario described. 
![collage](https://user-images.githubusercontent.com/50057221/58296326-47d72700-7da1-11e9-8ec0-e1d5ca7b29b3.jpg)

For this instance of image recognition, it is easily determined whether someone is wearing glasses without the use of color, so color information from each image can be durastically simplifed to greyscale. Where Each pixel represents an intensity scale from white to black.

![None_Fullres_Greyscale](https://user-images.githubusercontent.com/50057221/58293097-2cb0eb00-7d92-11e9-981f-57bb32074f68.jpg)

Additionally, image recognition can be done with many fewer pixels, just as someone can identify images that are not extremely pixel dense. Using Greyscale, and scaled-down images for Neural Network durastically decreases the computational power required, without having adverse effects on the network accuracy. 

![None_Scaledres_Greyscale_larger](https://user-images.githubusercontent.com/50057221/58294113-510ec680-7d96-11e9-823a-55f8b3cf3b81.jpg)

Now that the images are in a more simple format, They must be rearranged to enter into the neural network. Just as an image is a matrix of a NXM pixels of greyscale, or RGB values, that matrix can be reorganized into a 1X(MXN) Column. and this is the general input we will use for this network. In this case where each input pixel, and it's associated greyscale value, is the first "layer" of the NN

An Example  layout of a neural network is shown below
![Slide1_crop](https://user-images.githubusercontent.com/50057221/58295146-b44f2780-7d9b-11e9-8abd-4849b2009c50.jpg)

This is the actual MATLAB output of the Network, which uses 10 hidden layers, 
![ViewNN](https://user-images.githubusercontent.com/50057221/58296572-3e01f380-7da2-11e9-9243-cf87fea25771.JPG)

This is the output confusion matrix resulting from the network
![confusmatrix](https://user-images.githubusercontent.com/50057221/58297004-085e0a00-7da4-11e9-8fe7-d8a4b5743a0b.jpg)

The last section of the code allows for new input images for the network to be tested and outputs a guess, which is the highest classification accuracy Corresponding to the following
  - [1;0;0] = Nike
  - [0;1;0] = Ray Bans
  - [0;0;1] = No Glasses
  These results can also be interpreted to more simple "glasses" or "no glasses" result and not determine which specific sunglasses frame is being worn.

