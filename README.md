# tensorflow-gpu-install
cuda 8.0安装</br>
```
ssh zh@10.18.125.30</br>
sudo add-apt-repository ppa:graphics-drivers/ppa</br>
sudo apt-get update</br>
sudo apt-get install nvidia-375</br>
sudo apt-get install libcupti-dev</br>
sudo sh cuda_8.0.44_linux.run</b>
sudo vim /etc/profile</br>

export PATH=/usr/local/cuda-8.0/bin${PATH:+:${PATH}}</br>
export LD_LIBRARY_PATH=/usr/local/cuda-8.0/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}</br>
```
OR</br>
```
cd /etc/ld.so.conf.d/</br>
```
```
vim cuda-8-0.conf
```
modified follow:  
```
/usr/local/cuda-8.0/lib64
```  
```
sudo ldconfig  
tar -zxvf cudnn-8.0-linux-x64-v5.1.tgz  
sudo cp cuda/include/cudnn.h /usr/local/cuda/include/ && sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64/</br>

sudo chmod a+r /usr/local/cuda/include/cudnn.h && sudo chmod a+r /usr/local/cuda/lib64/libcudnn*</br>
```


PS:
```
sudo sh cuda_8.0.44_linux.run
```
驱动安装选择NO</br>

修改：
nano .bashrc</br>
vim .bashrc</br>
source ~/.bashrc</br>
# pip 安装 douban
vim /etc/pip.conf</br>

[global]</br>
index-url = http://pypi.douban.com/simple/ </br>
trusted-host = pypi.douban.com</br>
