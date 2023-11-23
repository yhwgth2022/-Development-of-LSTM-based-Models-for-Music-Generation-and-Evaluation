# Development of LSTM based Models for Music Generation and Evaluation

## Critic Model:

Problem Addressed:

This code segment demonstrates the application of a deep learning model, Critic, to solve the binary classification problem of musical sequences. The goal is to differentiate between "good music" and "bad music", essentially judging the quality of music based on its sequential data.

Method Used:

Model Design: Implemented a LSTM (Long Short-Term Memory) neural network model named Critic for processing sequence data. The model includes an LSTM layer and a fully connected layer, along with a BCEWithLogitsLoss loss function for binary classification.
Data Preparation: Transformed good and bad music data into tensors and assigned corresponding labels (1 for good music, 0 for bad music). The dataset was then split into training, validation, and test sets.
Training Process: The model was trained on the training set, including forward propagation, loss calculation, backpropagation, and parameter updates.
Validation Process: Evaluated the model's performance on the validation set, calculating validation loss and accuracy.
Testing Process: Conducted a final performance assessment on the test set, using the model to predict each sequence and calculating the overall accuracy.
Results Obtained:

On the test set, the model successfully made correct predictions for 1579 out of 2093 samples, achieving a classification accuracy of 75.44%.

## Composer Model:

The code for the Composer model aims to solve the problem of automatic music generation. The model is designed to generate musical sequences based on input data, representing a creative application of deep learning in the field of music.

Method Used:

Model Architecture: Implemented a Composer class, an LSTM-based neural network model, which is well-suited for sequential data like music. The model includes:
A multi-layer LSTM network for processing sequences.
A fully connected layer for output generation.
The forward pass method for defining the data flow through the model.
A method for initializing the LSTM's hidden and cell states.
A compose method for generating music sequences based on a starting note.

The output indicates the loss for each batch, which measures how well the model's predictions match the target sequences.
Sample loss values like 3.3385, 3.3464, etc., are observed during the eighth epoch, indicating the model's performance at that stage of training.

## Using Critic to evaluate Composer:

For 50 iterations, the code generates a sequence of music starting with a random note. This note is selected within the range of the maximum value in good_music_tensor.
Each generated sequence by the Composer is transformed into a tensor format suitable for the Critic model.
The Critic model then evaluates each generated sequence, providing a score that reflects the quality of the sequence as perceived by the model.








