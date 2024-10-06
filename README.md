Dataset: The MNIST dataset is loaded, containing handwritten digits from 0 to 9. Each image is 28x28 pixels, grayscale. Preprocessing:

The pixel values of the images are normalized (scaled to values between 0 and 1).

The images are reshaped to include a channel dimension, necessary for TensorFlow's CNN input.

The labels are one-hot encoded, meaning they are converted into binary vectors, each representing a class (digit). Model Architecture:

The model is a sequential CNN built using TensorFlow's Keras API.

The model starts with two convolutional layers followed by a max-pooling layer for downsampling and dropout layers for regularization to prevent overfitting.

After flattening the output, the model adds a fully connected (dense) layer and another dropout layer.

The output layer uses softmax activation to predict the class of the input image.

Training: The model is compiled with the Adam optimizer and trained using categorical cross-entropy as the loss function. It trains for 5 epochs with a batch size of 64. Both training and validation accuracy and loss are tracked.

Evaluation: The model is evaluated on the test set, achieving a high accuracy (99.09%). Visualization:

Two plots are generated: one for training and validation accuracy and another for training and validation loss across the 5 epochs.
