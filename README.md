# tensorflow-gpu-install
cuda 8.0安装</br>
ssh zh@10.18.125.30

sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt-get update
sudo apt-get install nvidia-375
sudo apt-get install libcupti-dev

sudo sh cuda_8.0.44_linux.run
sudo vim /etc/profile

export PATH=/usr/local/cuda-8.0/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-8.0/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}

tar -zxvf cudnn-8.0-linux-x64-v5.1.tgz
sudo cp cuda/include/cudnn.h /usr/local/cuda/include/ && sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64/

sudo chmod a+r /usr/local/cuda/include/cudnn.h && sudo chmod a+r /usr/local/cuda/lib64/libcudnn*



PS:
sudo sh cuda_8.0.44_linux.run 驱动安装选择NO

修改：
nano .bashrc
vim .bashrc
source ~/.bashrc
