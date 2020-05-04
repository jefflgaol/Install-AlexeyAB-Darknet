# Install-AlexeyAB-Darknet
## Step 1: Clone Darknet
```
$ cd ~
$ git clone https://github.com/AlexeyAB/darknet
$ cd darknet
```
## Step 2: Modify Makefile
```
$ gedit ~/darknet/Makefile
```
Make sure you have this configuration:
```
GPU=1
CUDNN=1
CUDNN_HALF=0
OPENCV=1
AVX=1
OPENMP=1
LIBSO=0
ZED_CAMERA=0 # ZED SDK 3.0 and above
ZED_CAMERA_v2_8=0 # ZED SDK 2.X

ARCH= -gencode arch=compute_61,code=compute_61
```
## Step 3: Install OpenCV library
```
$ sudo apt-get install libopencv-dev 
```
## Step 4: Make
```
$ make -j $(($(nproc) + 1))
```
