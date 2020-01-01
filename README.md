# 2D Face reconstruction using SFSNet using Tensorflow

This repository entirely reproduces the work done by Sengupta et. al. from University of Maryland and published in CVPR 2018. 
Please refer the [Project Page](https://senguptaumd.github.io/SfSNet/) and the [Github repo](https://github.com/senguptaumd/SfSNet) for further details. The algorithmic details can be found in the [paper](https://arxiv.org/pdf/1712.01261.pdf).

## Features
1. Face deconstruction - It provides the normal, shading, and albedo output for every input image. 
2. Face reconstruction - It reconstructs any given face using the normal, shading and albedo deconstruction results with variation in lighting if desired.
3. 3D face reconstruction - It inputs a 3D face and reconstructs it, with variations in lighting if desired. ( Work In Progress) 

## Installation and Usage

### Requirements
All the requirements can be found in the environment.yml file above. To install all the required dependencies and setup the environment to use,
```
conda env create -f environment.yml
source activate 3dface
```
### Data Loader
After the environment is setup, we require the datasets to be loaded, for the various training and testing steps. This data download and preparation can be done by,
```
python data_loader.py --skipnet_batch_size 10
```

Alternately, we can just run the ```setup.sh``` file to the same effect. Once the setup.sh file is run, the entire setup is complete. 

### Training module
In order to train the network we can simply run the ```run.sh``` file. This considers a set of default training parameters. The values can be changed to suit requirements using the training help. Training help can be found by running, 
```
python train.py --help
```

### Testing module
To be added


## Uninstallation

In order to just temporarily stop the environment and continue from the same point at a later stage we can instead use,
```
source deactivate 3dface
```
In order to purge the entire conda env and restart with this repo from the beginning please run,
```
purge.sh
```

