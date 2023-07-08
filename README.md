# Neural Style Transfer using TensorFlow

Neural Style Transfer is a technique that combines the content of one image with the style of another image to create a new artistic image. This repository provides an implementation of Neural Style Transfer using TensorFlow.

## Overview

The Neural Style Transfer process involves the following steps:

1. **Importing Dependencies**: TensorFlow, NumPy, Matplotlib, OpenCV, and Scipy libraries are required for this implementation.

2. **Model Setup**: The VGG19 model, pre-trained on the ImageNet dataset, is used as the feature extractor. The model's parameters are frozen to prevent training.

3. **Loading Images**: The content and style images are loaded and preprocessed. The images are resized to a desired height while maintaining the aspect ratio.

4. **Feature Extraction**: The loaded images are passed through the VGG19 model to extract features at specific layers. These features capture the content and style information.

5. **Gram Matrix Calculation**: The Gram matrix is computed for the style features. The Gram matrix represents the correlations between different channels of the feature maps.

6. **Loss Functions**: The content loss measures the difference between the target image's content features and the content image's features. The style loss measures the difference between the target image's style features and the style image's features. These losses help guide the optimization process.

7. **Optimization**: The target image, initially set as a copy of the content image, is optimized using the Adam optimizer. The optimization process aims to minimize the total loss, which is a combination of the content loss and style loss.

8. **Results**: The generated images at different stages of the optimization process are displayed, showcasing the gradual transformation from the content image to the stylized output.

## Usage

To use this implementation of Neural Style Transfer, follow these steps:

1. Install the required dependencies mentioned in the `requirements.txt` file.

2. Prepare your content and style images. Ensure that the images are compatible with the TensorFlow format and have the desired dimensions.

3. Adjust the parameters in the code, such as learning rate, alpha, beta, epochs, and show_every, to customize the optimization process.

4. Run the code and observe the output. The stylized image will be saved as "output_image.jpg" in the current directory.

## Results

The repository provides sample images demonstrating the transformation at different stages of the neural style transfer process. These images showcase the gradual blending of content and style to create the final stylized output.
