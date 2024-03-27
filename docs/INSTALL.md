# Installation

This codebase is tested on Ubuntu 20.04.2 LTS with python 3.8. Follow the below steps to create environment and install dependencies.

* Setup conda environment (recommended).
```bash
# Create a conda environment
conda create -y -n vclip python=3.7
# Activate the environment
source activate
conda activate vclip
# Install requirements
pip install requirements.txt
```

* Install Apex for enabling mixed-precision training.

NOTE: Make sure to have system CUDA of same version as of PyTorch CUDA version to properly install apex.
```
git clone https://github.com/NVIDIA/apex
cd apex
pip install -v --no-cache-dir --no-build-isolation --global-option="--cpp_ext" --global-option="--cuda_ext" --global-option="--deprecated_fused_adam" --global-option="--xentropy" --global-option="--fast_multihead_attn" ./
pip install -v --disable-pip-version-check --no-cache-dir --global-option="--cpp_ext" --global-option="--cuda_ext" ./
```
