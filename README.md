# DLIITKAI
Objective: Predicting tags using title and body of stack overflow questions

Programming Language: Ptyhon

Model architecture: Deep learning using RNN - LSTM

Data preprocessing:
Picked top 10 tags from the 'Tags' file
Used columns 'Id', 'Title', 'Body' from the Questions file, removed html tags using regex
Combined both Tags Questions file into one
Title and Body: Tokenize the owrds and convert it to sequences

Model building:
Used  Hybrid model in TensorFlow using Keras as high level. RNN has been used in the model. First train the model using 'Title' data, then train the same with 'Body' data. Combine both and passed through the dense layer before connect to the output layer.

The fully connected network has:
2 Dense layers
1 Dropout layers
1 BatchNormalization layer
1 Dense output layer Model Compilattion with optimizer = 'adam', loss = 'categorical_crossentropy', metrics='accuracy'

Model performance:
Classification report to check Precision, Recall and F1 Scroe

Saved the model (stackoverflow_tags.h5) in the below link for later use.
https://drive.google.com/open?id=1BnUs3r2tnjmFjWZaNo5AQ9kQxaKoiDDo&usp=drive_fs
