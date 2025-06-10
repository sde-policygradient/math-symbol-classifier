
# Math Symbol Classifier

## Contents

0. [Introduction](#introduction)
1. [Setup](#setup)

## Introduction

A simple image classification template originally designed to classify math symbols built on the Python Tensorflow API. It is designed with the intention to be as scalable as possible without much alteration to the source code.

## Setup

### Dependencies

Required dependencies:
- Python Standard Library
- MLCroissant (mlcroissant)
- RarFile (rarfile, unrar)
- Pillow (pillow)
- IPython (ipython)
- Jupyter widgets (ipywidgets)
- Tensorflow (tensorflow[and-cuda])
- NumPy (numpy)

> **Note**: This step is meant for Ubuntu. If you're using another distro, commands might be a bit different.

To install dependencies:
- PSL: `sudo apt install python3`
- Others: `sudo apt install unrar python3-pip && pip install mlcroissant pillow ipython ipywidgets tensorflow[and-cuda] numpy`

### Directories

- `croissants`: Croissants including dataset metadata.

### Variables

Find variables in `main.ipynb`, 3rd code cell
- `jsonld_path`: Path to a croissant containing metadata.
- `dataset_url`: URL to kaggle dataset.
- `load_image_dict`: Whether to load the image dictionary from the pickle referenced by `image_dict_pickle_path`. The pickle will be created if missing. If the pickle exists, it will be overwritten if this is set to `False`.
- `dataset_data_archive_path`: Path to an archive with directories of images.
- `image_dict_pickle_path`: Path to the pickle to load the image dictionary from.
- `dataset_shuffle_buffer_size`: Size of the buffer used in `tf.data.Dataset.shuffle`. Can either be `int` or `None`. If `None`, the full size of the dataset will be used. If not `None`, `dataset_shuffle_buffer_size` will be used.
- `train_split`: Fraction of the dataset to use for training, the rest will be used for evaluation.
- `dataset_batch_size`: Batch size used in `tf.data.Dataset.batch`
- `load_model`: Whether to load the model from from the file referenced by `model_path`. The file will be created if missing.
- `model_path`: Path to the file to load the model from.
- `model_init_hidden_layers`: The hidden layers the model will be initialized with if `load_model` is set to `False`.
- `train_epochs`: Number of epochs to train the model for.
