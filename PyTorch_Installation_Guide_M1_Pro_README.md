
# PyTorch Installation Guide for M1 Pro Mac

This guide provides instructions on how to install PyTorch on a Mac with an M1 Pro chip.

## Prerequisites

Before you begin, ensure that you have the following:

- A Mac with the M1 Pro chip.
- Homebrew installed. If not, you can install it from [Homebrew's website](https://brew.sh/).

## Step 1: Install Miniforge

Miniforge is a minimal installer for conda specifically tailored to conda-forge, and it's better suited for the M1 chip compared to Anaconda.

1. Install Miniforge for ARM64 architecture from the [Miniforge GitHub page](https://github.com/conda-forge/miniforge#miniforge3).
2. Open a terminal and run the installation script:
   ```bash
   bash Miniforge3-MacOSX-arm64.sh
   ```
3. Follow the prompts on the installer screens.

## Step 2: Create a Conda Environment

It's a good practice to create a separate environment for your PyTorch project.

1. In the terminal, create a new environment. For example:
   ```bash
   conda create -n pytorch_env python=3.8
   ```
   Here, `pytorch_env` is the environment name, and `python=3.8` specifies the Python version.

2. Activate the new environment:
   ```bash
   conda activate pytorch_env
   ```

## Step 3: Install PyTorch

Install PyTorch with the necessary dependencies.

1. Run the following command to install PyTorch:
   ```bash
   conda install pytorch torchvision torchaudio -c pytorch
   ```
2. This command will install the CPU-only version of PyTorch that's compatible with the M1 chip.

## Step 4: Verify the Installation

Ensure that PyTorch is installed correctly.

1. In the Python interpreter, run:
   ```python
   import torch
   print(torch.__version__)
   print("Is CUDA available:", torch.cuda.is_available())
   ```

## Conclusion

You should now have PyTorch installed on your M1 Pro Mac. For more information and advanced configurations, refer to the [official PyTorch website](https://pytorch.org/).
