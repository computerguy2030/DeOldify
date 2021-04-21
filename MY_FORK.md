# MY\_FORK

I am forking this repo to give instructions on using DeOldify on AMD hardware via the ROCm platform.

Note: Getting DeOldify to work on AMD cards is difficult and you may need to play arround with the various requirements for it to work.

## Instructions:

1. Install ROCm

2. Install Pytorch

3. Install vision

4. Install fast.ai

- Clone fastai
- git checkout fastai

5. Test DeOldify

- Clone DeOldify
- Install prerequisites (tensorboardX and jupyter lab)
- Start jupyter lab and monitor GPU usage

### 1. + 2. Install ROCm + Pytorch

I have created a script to install ROCm and Pytorch; however, since its completion, Pytorch released an official pip package you can use. I have not tried this, but it should work. Make sure to use the &quot;ROCm&quot; option in Pytorch.

Official release:

[https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)

My Script:

- git clone https://github.com/computerguy2030/pytorch-rocm-amd.git
- cd pytorch-rocm-amd
- bash amd\_build\_script.sh

### 3. Install vision

- git clone https://github.com/pytorch/vision.git
- sudo python3 setup.py install

### 4. Install fast.ai 
I have created a fork of the fast.ai repo and reverted changes to the required v1.0.51 for DeOldify:
git clone https://github.com/computerguy2030/fastai1.git

Original: <br>
Clone:

git clone https://github.com/fastai/fastai1.git

Checkout the correct version as advised by DeOldify:

git checkout c6bae03a697df565e9d30877069d41a6b813d98a

Install:

sudo python3 setup.py install

### 5. Start DeOldify Fun!!

Clone:

git clone https://github.com/jantic/DeOldify.git

Install prerequisites:

pip3 install jupyterlab tensorboardX

Start Jupyter Lab and that you are using GPU not CPU

- Run rocm-smi to check power draw, temp and other information
- Use radeontop to check GPU utlization

These tools should allow you to monitor your GPU to ensure the your code in the Jupyter Lab is executing on your AMD GPU.

### 6. Have fun!!!

jupyter lab

I have found much interesting B+W footage on archive.org and recommend it as a video and image source for your experiments.
