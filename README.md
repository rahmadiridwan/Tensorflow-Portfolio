# Tensorflow-Portfolio
Deep learning Tensorflow Keras projects in Image Classification and NLP

# Rock, Paper, Scissors Hand Gestures Image Classification Project ()
This is my first ever project using the Tensorflow Keras library as part of a machine learning course I took in Dicoding. The first task assigned in the course was to build a neural network using the Tensorflow Keras library to classify images of "rock, paper and scissors" hand gestures
* The raw dataset contains over 2188 sample pictures of rock, paper and scissors hand gestures (of roughly equal amount for each)
* An ImageDataGenerator is deployed for augmentation purposes (to reduce bias in the training process)
* A sequential model consisting of 3 convolutional hidden layers (consisting of a 2 dimensional convolution layer and a max pooling layer) followed by a hidden dense layer (after flattening the output of the convolutional layers) is constructed to train the classifier. Dropout layers set at a rate of 20% are also applied alternately after layers to prevent overfitting.
* A callback API, ReduceLROnPlateau is also implemented before compiling the model to reduce the learning rate by a factor of 0.5 should the model 'plateaus' (or in other words, the learning rate stagnates)
* The model is compiled with the loss function and the optimizer set to be categorical crossentropy and adam respectively, whilst the metric evaluated being the accuracy
* The model is then fitted against the training along with the validation dataset for up to 15 epochs
* The model is shown to be effective in producing a training accuracy of 96.35% and a validation accuracy of 95.88% 
* A function to classify an uploaded image of a hand gesture to be either as rock, paper or scissors called image_predictor is defined and applied to test the trained model

# NLP Text Classification of News Articles Project ()
This is my first NLP project with Tensorflow Keras and my second Tensorflow project overall. This is also a project which is part of the machine learning course I took in Dicoding and this is the second task that I was assigned 
* The dataset for this project is the BBC News dataset which consists of 2225 samples
* The first step taken was the removal of stopwords from the dataset (in order that common words which are not good indicators to classify the text data are not weighted in the training process)
* The text data and its labels are split into seperate training and validation sets using the sklearn train_test_split library
* The contents of the training and validation sets are then tokenized (limited to its 5000 most frequent words in the text training and validation set which includes an 'out of vocabulary' index)
* Padding is also applied to the text training and validation sets to produce sequences of the tokenized words in numpy arrays of equal lengths
* The label traing and validation sets are also tokenized and padded
* A sequential model consisting of an Embedding layer (to group the text data as vector representations based on its inclinations), a Bidirectional LSTM layer and an output dense layer is contructed along with a dropout layer set at a rate of 50%
* The model is compiled with the loss function and the optimizer set to be categorical crossentropy and adam respectively, whilst the metric evaluated being the accuracy
* The model is then fitted against the training along with the validation dataset for up to 12 epochs
* The model is shown to be effective in producing a training accuracy of 99.83% and a validation accuracy of 95.28% 
