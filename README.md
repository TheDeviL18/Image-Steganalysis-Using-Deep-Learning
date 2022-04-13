# Image-Steganalysis-Using-Deep-Learning

Steganalysis is the technology that attempts to defeat steganography by detecting the hidden information and extracting or destroying it. The carrier, stego-object and hidden message may be used when performing steganalysis. The goal of steganalysis is to identify suspected packages, determine whether or not they have a payload encoded into them, and, if possible, recover that payload. Steganalysis generally starts with a pile of suspect data files, but little information about which of the files, if any, contain a payload.

## Dataset
Alaska2 Dataset

The dataset used is named <a href="https://www.kaggle.com/competitions/alaska2-image-steganalysis/data">Alaska 2 Dataset.</a>

This dataset contains a large number of unaltered images, called the "Cover" image, as well as corresponding examples in which information has been hidden using one of three steganography algorithms (JMiPOD, JUNIWARD, UERD).

Each embedding algorithm is used with the same probability.
The payload (message length) is adjusted such that the "difficulty" is approximately the same regardless the content of the image. Images with smooth content are used to hide shorter messages while highly textured images will be used to hide more secret bits. The payload is adjusted in the same manner for testing and training sets.
The average message length is 0.4 bit per non-zero AC DCT coefficient.
The images are all compressed with one of the three following JPEG quality factors: 95, 90 or 75.

## Architecture
The network architecture used was a basic CNN model, with Max Pooling and ReLU Activation functions. Input images are resized to an optimal size and then fed into the Convolutional layer. These images are converted to their pixel values, which can be imagined as a three-dimensional matrix for the purpose of visualization. The Convolutional layer has a kernel. This kernel is generally a small matrix of specified kernel size mxnx3 (3 for RGB images). 

Rectified Linear Unit (ReLU) is the activation layer used in CNNs.The activation function is applied to increase non-linearity in the CNN. Images are made of different objects that are not linear to each other.

Max Pooling: A limitation of the feature map output of Convolutional Layers is that they record the precise position of features in the input. This means that small movements in the position of the feature in the input image will result in a different feature map. This can happen with re-cropping, rotation, shifting, and other minor changes to the input image. A common approach to addressing this problem from signal processing is called down sampling. This is where a lower resolution version of an input signal is created that still contains the large or important structural elements, without the fine detail that may not be as useful to the task.
