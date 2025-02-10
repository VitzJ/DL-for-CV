Assignment 1 for CS 698 Deep Learning For Computer Vision

HF Repo for generated dataset: https://huggingface.co/datasets/JohnVitz/DL_for_CV_Assignment_1

Assignment file .py: dl_for_cv_assignment_1_final.py
Assignment file .ipynb: DL_for_CV_Assignment_1_Final.ipynb

I had problems with the .ipynb file being either very large due to (I'm assuming) FiftyOne's session causing me to go over 25 mb for the notebook size.

Colab Notebook Link (editor perms): https://colab.research.google.com/drive/1qzQQYsXKvfYrX6ib2o5EKl6oGrADfJKR?usp=sharing

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
