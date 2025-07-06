
# Math Symbol Classifier

## Contents

0. [Introduction](#introduction)
1. [Setup](#setup)

## Introduction

A simple image classification template originally designed to classify math symbols built on the Python Tensorflow API. It is designed with the intention to be as scalable as possible without much alteration to the source code.

## Setup

This comes preconfigured for image classification on common math symbols.

### Dependencies

Required dependencies:
- Python Standard Library
- MLCroissant (mlcroissant)
- RarFile (rarfile, unrar)
- Pillow (pillow)
- IPython (ipython)
- Jupyter widgets (ipywidgets)
- Tensorflow (tensorflow[and-cuda])

To install dependencies for Ubuntu:
- PSL: `sudo apt install python3`
- Others: `sudo apt install unrar python3-pip && pip install mlcroissant pillow ipython ipywidgets tensorflow[and-cuda]`

### Variables

- `dataset_url`: URL to kaggle dataset.

- `jsonld_path`: Path to a croissant containing dataset metadata.
- `dataset_data_archive_path`: Path to an archive with directories of images relative to the dataset directory.
- `image_dict_pickle_path`: Path to the pickle to load the image dictionary from. The pickle will be created if missing. If it exists and `load_image_dict` is set to `False`, it will be overwritten.
- `model_path`: Path to the file to load the model from. The file will be created if missing. If the it exists, it will be overwritten.S

- `load_image_dict`: Whether to load the image dictionary from the pickle referenced by `image_dict_pickle_path`.
- `load_model`: Whether to load the model from from the file referenced by `model_path`.

- `image_display_resize`: Size to rescale images when displaying.
- `image_display_resampling`: Resampling method to use when displaying.
- `dataset_image_resize`: Size to rescale images when building dataset.
- `dataset_image_resampling`: Resampling method to use when displaying.

- `dataset_generator_shards`: Number of shards to use when building the dataset.
- `dataset_shuffle_buffer_size`: Size of the buffer used in `tf.data.Dataset.shuffle`. Can either be `int` or `None`. If `None`, the full size of the dataset will be used. If not `None`, `dataset_shuffle_buffer_size` will be used.
- `train_split`: Fraction of the dataset to use for training, the rest will be used for evaluation.
- `dataset_batch_size`: Batch size used in `tf.data.Dataset.batch`

- `model_init_hidden_layers`: The hidden layers the model will be initialized with if `load_model` is set to `False`.
- `early_stopping_patience`: The patience argument for the early stopping callback when training.
- `train_epochs`: Number of epochs to train the model for.
