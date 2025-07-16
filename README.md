NOTE: The Script's purpose is to set up VILA and perform a dry run restircted to one GPU.
      If you have more than one GPU you may adjust the align.sh & Train.sh scripts as needed

Pre-Installation Checklist:

1.	Enable WSL 2
Run these lines in PowerShell as an administrator:
wsl --install
wsl --set-default-version 2

2.	Install Ubuntu 22.04 (or 20.04) from Microsoft Store and open it at least once to finish initialization.

3.	Install the combined NVIDIA driver for Windows + WSL
Download from NVIDIA → “CUDA on WSL” package. 
Run: nvidia-smi inside WSL should show your GPU and CUDA version.

4.	Install Miniconda inside WSL
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
# allow it to add conda to ~/.bashrc

Once all the required software are installed, save and run the script stored in Environment_set_up to:
-	Refresh apt and install build tools
-	Install and activate your own Miniconda environment
-	Install PyTorch + CUDA and core libraries
-	Clone the VILA repository
-	Adjust the align.sh and train.sh scripts for having a singular GPU
-	Patch DeepSpeed zero3.json for CPU offload to prevent OOM errors
-	Perform the dry-run

Once the dry-run is successful you may run the full initialization script/begin training.
