# Introduction
main.py (run as python main.py) will pull in the images from the data/MNIST folder and train a multi-classification convolutional neural net to predict the image label given the 28x28 pixel source. The data/MNIST folder contains 60,000 training images and 10,000 testing images.

gui.py (run as python gui.py) will open up the user interface and allow user to 'write' in a digit using the mouse then will predict its label dynamically.  The gui.py will attempt to use the model recent model from the model/ folder so there must be at least a single model in that folder to run the GUI application. 

There are several parameters in the main.py file which can be changed to alter the runtime effects...


    LIMITED 			        = True # True if we want to restrict the data to 1000 images (debugging)
    LOAD 				        = True # True if we want to load a prior saved model
    VISUALIZE 			        = True # True if we want to view some results 
    VISUALIZE_TO_FILE 	        = True # True if we want to output the results to file rather than terminal
    TRAIN 				        = False # True if we want to retrain the net


## Installation

Dataset for the MNIST images located at http://yann.lecun.com/exdb/mnist/

Python (2.7) Modules: Keras, Theano/Tensorflow, PyQt4, NumPy, PyCuda

## GUI Prediction Examples
![Alt text](https://github.com/bfaure/Dynamic-Digit-Recognition/blob/master/data/screenshot_1.png)
![Alt text](https://github.com/bfaure/Dynamic-Digit-Recognition/blob/master/data/screenshot_2.PNG)
![Alt text](https://github.com/bfaure/Dynamic-Digit-Recognition/blob/master/data/screenshot_3.PNG)
![Alt text](https://github.com/bfaure/Dynamic-Digit-Recognition/blob/master/data/screenshot_4.PNG)

## MNIST Image Parser

The process I used to parse out the images from their files is restricted mostly to the data.py file. By default the data.py program will only parse out the first 1000 or so images and labels but this can be changed by setting the `limit` variable to false. Under this cirumstance the program will attempt to parse out all of the images and labels provided in the load_data parameters.
