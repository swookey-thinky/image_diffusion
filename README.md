# Image Diffusion

[![python](https://img.shields.io/badge/Python-3.9-3776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org)
[![pytorch](https://img.shields.io/badge/PyTorch-2.0.0-EE4C2C.svg?style=flat&logo=pytorch)](https://pytorch.org)

Small image diffusion implementation using latest research papers. Built for testing on small datasets, but extensible to large datasets given enough GPU.

This repository takes all of the learnings from the lessons at [Zero-to-Hero - Image Diffusion](https://github.com/swookey-thinky/mindiffusion/) and builds a single implementation to support them. This was born out of the realization that all of the image diffusion research is built upon the same fundamentals, and so in order to play out with those fundamentals and pieces, it was necessary to create a single repository to make it wasy to do so. This also makes the lessons above easier to implement since we can configure everything via YAML files.

This respository is built for experimentation, research, and fun. It has not been designed with efficiency or production in production in mind. However those are interesting topics in their own right, and we will probably explore those a little later.

## Setting Up Your Environment

All lessons are built using PyTorch and written in Python 3. To setup an environment to run all of the lessons, we suggest using conda or venv:

```
> python3 -m venv image_diffusion_env
> source image_diffusion_env/bin/activate
> pip install --upgrade pip
> pip install -r requirements.txt
> export PYTHONPATH=$(pwd)
```

All lessons are designed to be run *in the root of the respository*, so make sure to add the root of the repository to your `PYTHONPATH`, as in the above steps.

## Training

To train a model, you simply need a configuration file. You can find lots of examples of configuration files in the [configs](https://github.com/swookey-thinky/image_diffusion/configs) directory. For example, to train a basic DDPM-based, epsilon parameterized, unconditional diffusion model, run:

```
> python training/mnist.py --config_path configs/mnist/ddpm_unconditional_epsilon.yaml
```
