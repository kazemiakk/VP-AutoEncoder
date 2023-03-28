# VP-AutoEncoder
Map Velocity to Pressure for arterial stenosis using CFD data by Autoencoder with Pytorch
This project provides a Python script for creating an Autoencoder deep learning model with PyTorch to predict the variable P from input Vx, Vy, and Vz for CFD data from Ansys Fluent. The script includes a data loader to import 75 data for each point for Vx, Vy, and Vz and use them as input for the Autoencoder, with P as the output. The data is split into train data, validation data, and test data so that 20 percent test, 80 percent training, and 10 percent validation data are used.
