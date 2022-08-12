# cs523_sum2022

## Acknowledgements
This repository is adapted from https://github.com/oarriaga/face_classification

As a class project, we modify some of the codes.


## To see all the demos we've done
Please see folder "face_classification/test_images"

## Important Instructions to Set the Working Directory
In each of the ipynb files that you're going to run:

1. If you see "from google.colab import drive, drive.mount('/content/drive')", please follow the instruction in pop up window and allow the access
2. If you see "sys.path.insert(0,'/content/drive/My Drive/CS523/Project/face_classification/src')", please change this directory to where the "src" file existing in your won drive
3. If you see "%cd /content/drive/My Drive/CS523/Project/face_classification/src", please also change this directory to where the "src" file existing in your won drive

These should be in first 4 or 5 cells of each ipynb file.


## To Reproduce Model:
Google Drive Link: https://drive.google.com/drive/folders/11wvw-FcFqc16E5ZYBNSI_rWuUaZYpyqH?usp=sharing

Please download the google drive folder, upload it to you own google dirve, and run every ipynb files in colab.

Google Colab has all of the requirements installed (except scipy==1.2.1, but we have wrote this in the first cell of each ipynb file)

Then follow the instructions below:


## An Introduction to how to use the trained models

In folder "trained_models", all of the trained models are stored here. In the following instructions you can also change the path to store models.

We trained models using 2 residual modules by ourselves and store them in reduced_modules_experiments_2.

We trained models using 3 residual modules by ourselves and store them in reduced_modules_experiments_3.

We trained models using 4 residual modules by ourselves and store them in model_training_experiments.

We trained models using 5 residual modules by ourselves and store them in increased_modules_experiments_5.

The model provided by the paper is stored in emotion_models.
 
In the following instructions, please just change the paths of these models to use them. We've already chose the best ones from all of the models in each folder.
 
	 
## To train the Model in colab:
1. In src/models/cnn.py, find "mini_XCeption", and comment/uncomment the residual modules to modify the model (it's easy to find so take a look)
2. open "train_emotion_classifier.ipynb" in folder "src"
3. if you are having an error when running the cell contains "from keras.models import *", just re-run this cell, and it will work
4. change the variable "base_path" to decide where you want to store your models
4. Run all the code cell, then the training will starts. 
5. Accuracy and loss plot will be produced in the end 

## To Test the model:
0. upload the image you want to test to folder "images" in floder "face_classification"(if needed)
1. open "image_emotion_classifier.ipynb" in floder "src"
2. in the 4th cell, comment/uncomment the variable "emotion_model_path" to choose which trained model you'd like to use
3. if you are having an error when running the cell contains "from keras.models import *", just re-run this cell, and it will work
4. in the last cell, change the output path and the output image name that you'd like to have
5. run all the code
6. please check the output image in the path you just entered

## To reproduce the confusion matrix:
1. In src, open "confusion_matrix.ipynb"
2. change the variable "emotion_model_path" to the desired model
3. run the code
4. all of the confusion matrix are already displayed, but feel free to redraw
