# Public-NN-Rocket-Code
Downloads to support API Hub service for Time Series Classification

Starting from the sample code of the Time Series Classification provided by the IBM development team, the code will use the public IBM service to understand the service's function and parameter configuration.

Currently, the source code allows the analysis of a dataset in CSV format. The parameters used to analyze the CSV dataset should be provided on a .csv.params file. The parameter file format is JSON. 
For example, to analyze the dataset01.csv file, you have to specify the parameters on dataset01.csv.params file. 

Following, a sample of params file

    {
        "time column": "Time",
        "time string format": "%Y-%m-%d %H:%M",
        "target columns": "[\"Value1\",\"Value2\",\"Value3\"]",
        "categorical columns": "['Category1','Category2','Category3']",
        "label column": "Label",
        "snapshot column": "Snapshot",
        "train test split": "0.5",
        "result type": "all"
    }

This change allows using the Jupiter notebook source code, avoiding any change in the source code. 
# How to run the source code locally
If you like to use the source code locally you can use Visual Studio Code adding the Jupyter Extension.
# How to set IBM credentials
To use this code you have to set the IBM credentials on .env file like the following

    IBM_CLIENT_ID=<your ibm client id>
    IBM_CLIENT_SECRET=<your ibm client secret>

If you don't want to use .env file you have to set IBM credentials on:

    my_id = "<your ibm client id>"
    my_secret = "<your ibm client secret>"
