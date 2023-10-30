
# SincNet
This is a still under development adaptation of the [SincNet](https://github.com/mravanelli/SincNet).

## Prerequisites
- Python 3.6
- Pytorch
- Soundfile


## Suggested preparation steps for beginners
If you are not a beginner, you can skip this section and go straight to "How to run" section.

Use a LINUX distro. I recommend Ubuntu or an Ubuntu-based distro. If you have Windows, you can use WSL to install Ubuntu or another LINUX distro of your choice. For simplification purposes, I will assume you are using a fresh installed Ubuntu system and you have at least one NVIDIA GPU card.

1. Update and upgrade your system.
```bash
sudo apt update && sudo apt upgrade -y
```

2. Install git and sox.
```bash
sudo apt install -y git sox
```

3. Download and install [CUDA](https://developer.nvidia.com/cuda-downloads).

4. Download and install Miniconda, then initialize the base environment.
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```
```bash
bash Miniconda3-latest-Linux-x86_64.sh
```
```bash
source ~/.bashrc
```

5. Create a new conda environment for sincnet using Python 3.6, then activate it.
```bash
conda create -n sincnet python=3.6
```
```bash
conda activate sincnet
```

6. Install Pytorch and Soundfile
```bash
conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
```
```bash
conda install -c conda-forge pysoundfile
```

7. Clone SincNet repository from Github, go to SincNet folder, create "models" folder, and give permissions to execute .sh files.
```bash
git clone https://github.com/tito-spadini/SincNet
```
```bash
cd SincNet
```
```bash
mkdir models
```
```bash
chmod +x *.sh
```

Now you are able to run SincNet.


## How to run
Update TIMIT_PATH on prepare.sh and run it.
```bash
./prepare
```

Check if cfg/SincNet_TIMIT.cfg is using the desired configs, then run train.sh.
```bash
./train
```