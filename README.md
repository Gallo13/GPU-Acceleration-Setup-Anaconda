# GPU-Acceleration-Setup-Anaconda
GPU Acceleration Setup for Anaconda (Tensorflow)

* This assumes you have Anaconda already installed on your computer

Steps:
1) Make sure your computer has a GPU
    * I. Open Task Manager
    * II. Click Performance
    * III. You will see GPU 1 where the GPU is: 
    ![image](https://user-images.githubusercontent.com/54815820/140799800-048e83fb-8dfe-4ae0-b81f-d283c478010b.png)
2) Install CUDA onto your computer
    * I. To know which version of CUDA to install, open CMD (Win+R -> cmd), in CMD write nvidiam-smi. It will give you this: 
    ![image](https://user-images.githubusercontent.com/54815820/140800610-a6c2bc94-7d1b-4914-a75c-29fe762e2186.png)
    * II. Where it says CUDA Version: 11.4, that is the newest version of CUDA your GPU use.
3) Install cuDNN onto your computer
    * I. You can base which cuDNN version to download on which CUDA version you downloaded
4) Check to make sure CUDA and cuDNN are installed
    * I. Open CMD, type nvcc --version 
    ![image](https://user-images.githubusercontent.com/54815820/140802208-5088f9d3-790d-4174-bcf7-758c59938174.png)
5) Install Visual Studio
---------------------------------------------------------------------------------------------------------------------
6) Create a new evironment in Anaconda
    * I. Open Anaconda and type: create --name tensorflow
    * This creates a new virutal environment called tensorflow
7) Access environment
    * I. Type: conda activate tensorflow
8) Install Python
    * I. type conda install python='version'
    * The pyton version you install on this environment depends on the tensorflow version you need
---------------------------------------------------------------------------------------------------------------------
OR
6) Create a new environment with python altogether
   * Type: conda create --name tensorflow python=3.8
   * Then: conda activate tensorflow
   * Last: conda install -c conda-forge nb_conda (for Jupyter support)
---------------------------------------------------------------------------------------------------------------------
9) Install CUDA Toolkit and cuDNN
    * I. type: conda install -c anaconda cudatoolkit='version'
10) Install tensorflow-gpu
    * I. type: conda install -c anaconda tensorflow-gpu
11) Install Jupyter Notebook
    * I. type: conda install jupyternotebook
12) Register your environment
    * type: python -m ipykernel install --user --name tensorflow --display-name 'Tensorflow (Py3.8)'
