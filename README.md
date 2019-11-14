# EIP_4_Seesion_01

Print(Score)
[0.02730164076744113, 0.9901]

1. Convolution

Convolution is one of the main operations in CNN. The primary purpose of Convolution in CNN is to extract features from the input image. Convolution preserves the spatial relationship between pixels by learning image features using small squares of input data.

2. Filters/Kernels

A filter is an integral component of the CNN architecture. It acts as the feature detector from the original input image. It transforms the information encoded in the pixels from the input image.  In practice, however, a kernel is a smaller-sized matrix (above 3 x 3 matrixes) in comparison to the input dimensions of the image that consists of real valued entries. The real values of the kernel matrix change with each learning iteration over the training set.

3. Epochs

An epoch describes the number of times the algorithm sees the entire data set. So, each time the algorithm has seen all samples in the dataset, an epoch has completed.

If we have a dataset of 10 examples with a batch size of 2 and if we specified the algorithm to run for 3 epochs.

Therefore, in each epoch, we have 5 batches (10/2 = 5). Each batch gets passed through the algorithm; therefore we have 5 iterations per epoch. Since we've specified 3 epochs, we have a total of 15 iterations   (5 x 3 = 15) for training.

4. 1x1 Convolution

A 1x1 convolution simply maps an input pixel with all its channels to an output pixel, not looking at anything around itself. It is often used to reduce the number of depth channels, since it is often very slow to multiply volumes with extremely large depths.

Input (256 depth) -> 1x1 convolution (64 depth) -> 4x4 convolution (256 depth)

Input (256 depth) -> 4x4 convolution (256 depth)

5. 3x3 Convolution

The Convolution process of the input image with the 3 x 3 matrix (kernel) is termed as the 3 x 3 convolution. We slide the 3 x 3 kernel matrix over our original image by 1 pixel (also called ‘stride’) and for every position, we compute element wise multiplication (between the two matrices) and add the multiplication outputs to get the final integer which forms a single element of the output matrix ( feature map).

6. Feature Maps

The matrix formed by sliding the filter over the input image and computing the dot product is called the ‘Convolved Feature’ or ‘Activation Map’ or the ‘**Feature Map**‘. Activation maps indicate ‘activated’ regions, i.e. regions where features specific to the kernel have been detected in the input. Different values of the filter matrix will produce different Feature Maps for the same input image.

7. Activation Function

Human Brains sent a lot of signals if it got really exciting. The rate of emission of these signals tells us the intensity of the original stimulus. These are Human action and these are highly related to each other as stronger the signal higher the frequency of action to be taken.

Whole Ideology is that these potential Actions can be thought of Activations Functions in terms of Neural Networks. The path that needs to be fired depends on the activation functions in the preceding layers just like any physical movement depends on the action potential at the neuron level. The path that is needed to be taken depends on Activation Functions in the subsequent layers in the same way physical Movement depends on action at the neuron level.

The Main goal of Activation function is to convert the input signal of a node in Artificial Neural Nets to the output signal. The Output Signal from this node will be used as input to the Next layer in Stack.

8. Receptive Field

The receptive field is defined as the region in the input space that a particular CNN’s feature is looking at (i.e. be affected by). A receptive field of a feature can be described by its center location and its size. However, not all pixels in a receptive field is equally important to its corresponding CNN’s feature. Within a receptive field, the closer a pixel to the center of the field, the more it contributes to the calculation of the output feature.
