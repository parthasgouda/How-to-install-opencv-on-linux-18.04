# How to install opencv on linux 18.04
Installation of latest version of opencv on linux

In order to install opencv on linux(ubuntu only) we need the following packages

1. Cmake(gui preferred)
2. OPENCV latest source code
3. OPENCV-contrib latest source code

### Installing CMAKE and CMAKE GUI:

1. Download the latest version of cmake(cmake-x.xx.x.tar.gz or cmake-x.xx.x.tar.Z) from  https://cmake.org/download/
2. Extract the contents of the file that was downloaded into a folder
3. Open terminal in the folder where the .tar.gz or .tar.Z was extracted to.
4. use the following commands: 
>./bootstrap --qt-gui

>make -j4

or

>make -j8

*Depending on the output for*
>nproc

Then, *cmake* can be *optionally* installed using the following command:
>make install 
        
#### Possible errors
One the possible errors from the above commands could be due to the absense of qt on the system. The following link can be followed to install qt 

https://wiki.qt.io/Install_Qt_5_on_Ubuntu

### Installing Opencv and Opencv-contrib

#### Install pre-requisites

>sudo apt-get install build-essential

>sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev

>sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev

#### Download the right version of Opencv and Opencv-contrib
1. Create a working directory for opencv

>cd ~/<my_working_directory>

>git clone https://github.com/opencv/opencv.git

>git clone https://github.com/opencv/opencv_contrib.git

2. Create a build folder 

>cd ~/opencv

>mkdir build

>cd build

3. Run cmake gui from the bin folder in CMAKE(if not installed in the system) or  

>cmake-gui

4. 
![alt-text] (Screenshot from 2019-04-05 14-36-47.png)

