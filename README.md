# VP-AutoEncoder
This project provides a Python script for creating an Autoencoder deep learning model with PyTorch to predict the variable P from input Vx, Vy, and Vz for CFD data from Ansys Fluent. The script includes a data loader to import 7500 data for each point for Vx, Vy, and Vz and use them as input for the Autoencoder, with P as the output. The data is split into train data, validation data, and test data so that 20 percent test, 80 percent training, and 10 percent validation data are used.

VP-AutoEncoder

This project provides a Python script for creating an Autoencoder deep learning model with PyTorch to predict the variable P from input Vx, Vy, and Vz for Computational Fluid Dynamics (CFD) data from Ansys Fluent. The script includes a data loader to import 7500 data for each point for Vx, Vy, and Vz and use them as input for the Autoencoder, with P as the output. The data is split into train data, validation data, and test data so that 20 percent test, 80 percent training, and 10 percent validation data are used.

Requirements:
PyTorch
Pandas
NumPy
Scikit-learn
Matplotlib
Installation

To install the required packages, run the following command:

pip install -r requirements.txt

Usage

The script is divided into several sections, each of which can be run sequentially. Here’s a brief overview of what each section does:

Section 1: Load Data

This section loads the CFD data from Ansys Fluent in CSV format and prepares it for use in the Autoencoder model. The script reads in the CSV files for the spatial domain of each point and extracts the variables Vx, Vy, Vz, and P. The data is then concatenated and split into train data, validation data, and test data.

Section 2: Define Autoencoder Model

This section defines the architecture of the Autoencoder model using PyTorch. The model has three hidden layers with a bottleneck layer in the middle. The input layer takes the Vx, Vy, and Vz variables as input, and the output layer produces the predicted value of P.

Section 3: Train Autoencoder Model

This section trains the Autoencoder model using the train data and validation data. The script uses the Mean Squared Error (MSE) loss function to calculate the error between the predicted output and the actual output. The model is trained using the Adam optimizer with a learning rate of 0.001 and a batch size of 32.

Section 4: Test Autoencoder Model

This section tests the trained Autoencoder model using the test data. The script calculates the Area Under the Curve (AUC), training accuracy, testing accuracy, and validating accuracy in percentage and prints them for each epoch. The results are plotted for online monitoring of the training/testing.

License

This project is licensed under the MIT License - see the LICENSE.md file for details.
