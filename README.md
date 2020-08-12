[![minimal Python version](https://img.shields.io/badge/Python-3.6-6666ff)](https://www.anaconda.com/distribution/)

# NEUBIAS_chapter_DL_2020
This repository contains all the material for the chapter "Building a Bioimage Analysis Workflow using Deep Learning".

The proposed workflow makes use of open source software tools (Keras, DeepImageJ and MorphoLibJ) to segment and analyze the morphology of phase contrast images from the Cell Tracking Challenge.

## Worflow steps 
* **Steps 0 to 3** take place in a Python notebook (click to open the notebook in Google Colab: [![GoogleColab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/esgomezm/NEUBIAS_chapter_DL_2020/blob/master/notebook/U_Net_PhC_C2DL_PSC_segmentation.ipynb)) and are as follows:
  * **Step 0**: initialize the notebook in Google Colab to make use of a GPU runtime and set-up the correct Keras/Tensorflow versions.
  * **Step 1**: download, extract and partition the image data into training, validation and test sets.
  * **Step 2**: define and train a deep learning model for segmentation:
    * **Step 2.1**: prepare images for training.
    * **Step 2.2**: design a convolutional neural network (U-Net-like).
    * **Step 2.3**: define loss function and optimizer.
    * **Step 2.4**: train model.
  * **Step 3**: evaluate trained model in test set.
* **Step 4** starts at the end of the notebook and involves importing the train model into DeepImageJ:
  * **Step 4.1**: download the train model from the notebook in Tensorflow format.
  * **Step 4.2**: install DeepImageJ in ImageJ/Fiji.
  * **Step 4.3**: import model into DeepImageJ using "Create Bundled Model" plugin.
* **Step 5**: apply the trained model to all images in a folder using DeepImageJ from an ImageJ macro.
