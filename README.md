# GPU-Acceleration-Setup-Anaconda
GPU Acceleration Setup for Anaconda (Tensorflow)

* This assumes you have Anaconda already installed on your computer

Steps:
1) Make sure your computer has a GPU\n
    *I. Open Task Manager\n
    *II. Click Performance\n
    *III. You will see GPU 1 where the GPU is: \n
    ![image](https://user-images.githubusercontent.com/54815820/140799800-048e83fb-8dfe-4ae0-b81f-d283c478010b.png)\n
2) Install CUDA\n
    *I. To know which version of CUDA to install, open CMD (Win+R -> cmd), in CMD write nvidiam-smi. It will give you this: \n
    ![image](https://user-images.githubusercontent.com/54815820/140800610-a6c2bc94-7d1b-4914-a75c-29fe762e2186.png)\n
    *II. Where it says CUDA Version: 11.4, that is the newest version of CUDA your GPU use.\n
3) Install cuDNN\n
    *I. You can base which cuDNN version to download on which CUDA version you downloaded\n
4) Check to make sure CUDA and cuDNN are installed\n
    *I. Open CMD, type nvcc --version \n
    ![image](https://user-images.githubusercontent.com/54815820/140802208-5088f9d3-790d-4174-bcf7-758c59938174.png)\n
5) Install Visual Studio\n
6) Create a new evironment in Anaconda\n
    *I. Open Anaconda and type: create --name tensorflow\n
    *This creates a new virutal environment called tensorflow\n
7) Access environment\n
    *I. Type: conda activate tensorflow\n
8) Install Python\n
    *I. type conda install python='version'\n
    *The pyton version you install on this environment depends on the tensorflow version you need\n
9) Install CUDA Toolkit and cuDNN\n
    *I. type: conda install -c anaconda cudatoolkit='version'\n
10) Install tensorflow-gpu\n
    *I. type: conda install tensorflow=='version'\n
