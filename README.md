# VQA using CLIP model

This repository contains the code and data for the Visual Question Answering (VQA) project. The goal of VQA is to answer open-ended questions based on an image. This project utilizes the VizWiz dataset, which is specifically designed to train models to assist visually impaired individuals.

## Problem Statement

VQA has many applications: Medical VQA, Education purposes, for surveillance and numerous other applications. In this assignment we will use VizWiz dataset, this dataset was constructed to train models to help visually impaired people.

In the words of creators of VizWiz: "we introduce the visual question answering (VQA) dataset coming from this population, which we call VizWiz-VQA. It originates from a natural visual question answering setting where blind people each took an image and recorded a spoken question about it, together with 10 crowdsourced answers per visual question."

## Required Libraries

To run the code in this repository, the following libraries need to be installed:

-   ftfy
-   regex
-   tqdm
-   git+https://github.com/openai/CLIP.git
-   pytorch-lightning

```
! pip install ftfy regex tqdm --q --root-user-action=ignore
! pip install git+https://github.com/openai/CLIP.git --q --root-user-action=ignore
! pip install pytorch-lightning --q --root-user-action=ignore
```

The code also requires additional libraries:

-   numpy
-   skimage
-   torch
-   json
-   matplotlib.pyplot
-   pandas
-   pickle
-   clip
-   gc
-   nltk
-   inspect
-   tabulate
-   collections.Counter
-   PIL.Image
-   sklearn
-   pkg_resources.packaging
-   torch
-   pytorch_lightning

## Model Used

The model used for this project is based on the ViT-L/14@336px architecture, with an image size of 336x336.

## Dataset

The dataset used for this project is the VizWiz-VQA dataset, which contains 20,500 image/question pairs. Each image has its corresponding question and 10 answers to this question. The dataset is divided as follows:

-   Training Set:

    -   Number of image/question pairs: 20,523
    -   Number of answer/answer confidence pairs: 205,230

-   Validation Set:
    -   Number of image/question pairs: 4,319
    -   Number of answer/answer confidence pairs: 43,190

You can mount the data instantly without any hassle from [Kaggle](https://www.kaggle.com/datasets/lhanhsin/vizwiz) .

### Dataset Files

The following files are required for the dataset:

-   testing_images (pickle file)
-   testing_text (pickle file)
-   training_images (pickle file)
-   training_text (pickle file)
-   validation_images (pickle file)
-   validation_text (pickle file)

Make sure to adjust the directory paths in the code to match the file locations on your system:

```
DATA_DIR = "/kaggle/input/vizwiz/"
PICKLE_DIR = "/kaggle/input/vizwiz-pickle/"
MODEL_DIR = "/kaggle/input/vizwiz-model/"
```

## Contributors:

-   [Ahmad Hazem](https://github.com/AhmadHazem)
-   [Zeyad Zakaria](https://github.com/ZeyadZakaria01)
