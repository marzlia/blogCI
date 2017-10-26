---
title: 项目实践0x01 keras与tensorflow在windows下的部署
date: 2017-10-26 18:55:56
tags: tensorflow
---
[参考路径](https://github.com/antoniosehk/keras-tensorflow-windows-installation)
10 easy steps on the installation of TensorFlow-GPU and Keras in Windows

### 0x01 : 安装 Anaconda (Python 3.6 版本) 
<a href="https://www.continuum.io/downloads" target="_blank">下载</a>

![](https://raw.githubusercontent.com/antoniosehk/keras-tensorflow-windows-installation/master/cuda8_windows7_local_installation.png)

### 0x02: 升级 Anaconda
打开 Anaconda 软件运行以下的命令
```Command Prompt
conda update conda
conda update --all
```

### 0x03: 安装 CUDA Tookit 8.0 
<a href="https://developer.nvidia.com/cuda-downloads" target="_blank">下载</a>

选择你的操作系统对应的版本

![](https://raw.githubusercontent.com/antoniosehk/keras-tensorflow-windows-installation/master/cuda8_windows7_local_installation.png)

### 0x04: 下载 cuDNN 
<a href="https://developer.nvidia.com/rdp/cudnn-download" target="_blank">Download</a>

选择你对应操作系统的版本，此处需要注册才能下载。
![](https://raw.githubusercontent.com/antoniosehk/keras-tensorflow-windows-installation/master/cuDNN_windows_download.png)


解压到你所需要的磁盘目录下: 
```Command Prompt
C:\cudnn-8.0-windows10-x64-v5.1
```
### 0x05: 添加 cuDNN 到你的系统环境 PATH 中 
<a href="https://kb.wisc.edu/cae/page.php?id=24500" target="_blank">Tutorial</a>

在您的环境中添加以下路径。受到你的安装路径的变化。
```Command Prompt
C:\cudnn-8.0-windows10-x64-v5.1\cuda\bin
```

关掉所有的提示。打开一个新的 Anaconda 窗口输入以下命令
```Command Prompt
echo %PATH%
```
您应当看到新环境路径。

### 0x06: 创建一个 Anaconda 环境 Python=3.5
```Command Prompt
conda create -n tensorflow python=3.5 numpy scipy matplotlib spyder
```

### 0x07: 切换环境

```Command Prompt
activate tensorflow
```

### 0x08: 安装 TensorFlow-GPU-1.2.0

```Command Prompt
pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/windows/gpu/tensorflow_gpu-1.2.0-cp35-cp35m-win_amd64.whl
```

### Step 9: 安装 Keras

```Command Prompt
pip install keras
```

### Step 10: 测试
去下载以下实例进行测试 <a href="https://raw.githubusercontent.com.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/examples/mnist_mlp.py">mnist_mlp.py</a> 


```Command Prompt
activate tensorflow
python mnist_mlp.py
```
恭喜 ! 你成功的在widows下利用GPU运行 Keras (with Tensorflow backend)  !
![](https://raw.githubusercontent.com/antoniosehk/keras-tensorflow-windows-installation/master/installation_success.png)