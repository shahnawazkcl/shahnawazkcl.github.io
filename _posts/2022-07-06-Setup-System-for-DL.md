---
layout: post
title: Setup system for deep learning
description: simple guide tosetup ubuntu system for deep learning with cuda.
date: 2022-07-06
tags: deeplearning

---
# Setup your system for Deeplearning  

Hello, there fellow deep learners. I am writing this blogpost to not only document how I did setup my system for running deep learning algorithms but also to make it easy for others to understand How to.  
In this blog post, I am going to take you through steps involved in setting up your __Ubuntu20.04__ system for running Deep Learning models. In the due course I promise to make it as simple as possible with some insights along the way.  

> *Disclaimer: If you are an expert in any of the concepts, steps or terms discussed here, then please do comment or correct me. Although here my only goal is to make and keep it __simple__.*

So, without furthure due __Lets start__.....!

> __As obvious sometimes simple things seems impossible but with fair amount information they can be made easy...!__

Thus lets set up your Linux system for running deep learning which can seem like a daunting task, but with a few simple steps, you can have everything up and running in no time.

## Step 1: Update and Upgrade your system

Before installing any new software, it's always a good idea to update and upgrade your system. This ensures that you have the latest security updates and bug fixes. Open a terminal and run the following commands:

    sudo apt-get update 
    sudo apt-get upgrade

## Step 2: Install NVIDIA Drivers

Deep learning requires a powerful GPU, and the most popular choice for this is NVIDIA. To install the NVIDIA drivers, you'll first need to determine which GPU you have. You can do this by running the following command in the terminal:

    lspci | grep -i nvidia

This will give you the model of your NVIDIA GPU. Once you know the model, you can install the appropriate drivers. For example, if you have a NVIDIA GeForce GTX 1080, you would run the following command:

    sudo apt-get install nvidia-390

## Step 3: Install CUDA and cuDNN

CUDA is a parallel computing platform and programming model developed by NVIDIA for general computing on GPUs. cuDNN is a GPU-accelerated library of primitives for deep neural networks. To install CUDA and cuDNN, you'll need to register for a free NVIDIA developer account and download the appropriate versions for your system. The link can be find [here](https://www.nvidia.com/download/index.aspx)

## Step 4: Install Anaconda

Anaconda is a distribution of Python and R for scientific computing and data science. It comes with a lot of useful packages pre-installed, including Jupyter Notebook, which is a great tool for deep learning. To install Anaconda, download the appropriate version for your system from the Anaconda website and run the installer. [Follow this for step by step guide](https://docs.anaconda.com/anaconda/install/linux/), once you have installed move on to next step.

## Step 5: Create a conda environment

A conda environment is a separate Python environment that allows you to install packages without interfering with the system-wide Python installation. To create a conda environment, open a terminal and run the following command:

    conda create --name deeplearning

> Replace "deeplearning" with the name of your choice. I like to name environments based on projects.

## Step 6: Activate the conda environment

In order to install the required packages we need to activate the enviroment first to activate the conda environment, run the following command:

    conda activate deeplearning

## Step 7: Install TensorFlow and Keras

TensorFlow is an open-source deep learning framework, and Keras is a high-level neural networks API that runs on top of TensorFlow. To install TensorFlow and Keras, run the following command:

    conda install tensorflow-gpu keras

## Step 8: Install other necessary packages

There are other packages that are commonly used in deep learning, such as NumPy, SciPy, and Matplotlib. To install these packages, run the following command:

    conda install numpy scipy matplotlib

That's it! Your system is now set up for running deep learning. You can start experimenting with different models and techniques using Jupyter Notebook or your preferred Python IDE.

Keep in mind that the above steps are just a guide and you should adjust the commands accordingly. Also, If you're using a different version of Ubuntu or have a different version of NVIDIA GPU, the commands and version numbers may be different.
