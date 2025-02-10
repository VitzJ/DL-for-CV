Assignment 1 for CS 698 Deep Learning For Computer Vision

HF Repo for generated dataset: https://huggingface.co/datasets/JohnVitz/DL_for_CV_Assignment_1
Colab Notebook Link (editor perms): https://colab.research.google.com/drive/1qzQQYsXKvfYrX6ib2o5EKl6oGrADfJKR?usp=sharing

Assignment file .py: dl_for_cv_assignment_1_final_revised.py
Assignment file .ipynb: DL_for_CV_Assignment_1_Final_Revised.ipynb

I had problems with the .ipynb file being very large due to (I'm assuming) FiftyOne's session loading picture previews for all of the images causing me to go over 25 mb for the notebook size. 
After reducing the size a bit, I utilized the "Save a Copy in Github" Feature with Colab, and realized that moving ipynb files to different directories as well as renaming them in github causes an nbconvert error in Github itself, which means that it doesn't show any results.

_______________________________________________________________

On Colab, Project requires pip installs:

!pip install datasets
!pip install huggingface_hub datasets
!pip install fiftyone

Required Imports:

import zipfile
import os
from datasets import load_dataset, DatasetDict
import matplotlib.pyplot as plt
from huggingface_hub import notebook_login
import glob
import torch
from torchvision import transforms
import requests
from io import BytesIO
from PIL import Image
import fiftyone as fo
import fiftyone.zoo as foz
import tempfile
import shutil
