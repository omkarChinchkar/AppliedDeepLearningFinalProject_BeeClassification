# Bee_Classification

# Task


To compare the performance of 3 layered convolutional neural network architecture and transfer learning approach for VGG19 model, with imageNet weights, on Bee classification task.

# Dataset

Both models were trained on Bee or wasp kaggle dataset. https://www.kaggle.com/jerzydziewierz/bee-vs-wasp

# Model discription

## CNN model:

keras sequential model design was used in this task. 3 convolutional blocks and classifier head are present in the model. 

### Convolutional Blocks:

First convolutional block has 128 filters with kernel size 5, padding is set to "same", activation function is "relu", input shape is (256,256,3).
Second convolutional block has 256 filters with kernel size 3, padding as "same" and "relu" activation function.
Third convolutional block has 516 filters with kernel size 3, padding as "same" and "relu" activation funcion.
maxPooling is done after each convolutional block.

### Classifier Head:

Dense 6 units with relu activation function and 1 unit with sigmoid activation funtion for bee classification.

### Optimizer: 

Adam with 0.1 epsilon

### Loss:

binary_crossentropy

### Metric:

binary_accuracy


## VGG19 model:

Keras VGG19 model weight for classification.

### Transfer Learning:

ImageNet weights are used for transfer learning approach. Input shape is (224,224,3), "softmax" classifier activation.

### Optimizer:

Adam with 0.0001 learning rate.

### Loss:

BinaryCrossentropy


# Results

### CNN model Results:
0.75 training and testing accuracy after 50 epochs.

### VGG19 model Results:
0.9250 validation accuracy and 0.9285 testing accuracy after 50 epochs.

# Dependancies
!pip install tensorflow

!pip install pandas

!pip install matplotlib

!pip install seaborn

