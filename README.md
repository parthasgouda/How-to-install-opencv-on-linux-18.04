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
![cmake configuring](https://raw.githubusercontent.com/parthasgouda/How-to-install-opencv-on-linux-18.04/master/Screenshot%20from%202019-04-05%2014-36-47.png)

5. Click configure

6. Click finish

![setting up compiler](https://raw.githubusercontent.com/parthasgouda/How-to-install-opencv-on-linux-18.04/master/Screenshot%20from%202019-04-05%2014-55-01.png)

7. 

![To configure compiler](https://raw.githubusercontent.com/parthasgouda/How-to-install-opencv-on-linux-18.04/master/Screenshot%20from%202019-04-05%2015-01-18.png)

8. Add opencv-contrib folder to the cmake

![add contrib folder](https://raw.githubusercontent.com/parthasgouda/How-to-install-opencv-on-linux-18.04/master/Screenshot%20from%202019-04-05%2015-08-26.png)

9. Configure for opencv-contrib

![configure for opencv-contrib](https://raw.githubusercontent.com/parthasgouda/How-to-install-opencv-on-linux-18.04/master/Screenshot%20from%202019-04-05%2015-17-03.png)

10. click configure and then generate.

11. After the make file has been generate. Use the following commands in the terminal with build folder(which was created in step 2) as working directory.


>make -j4

or

>make -j8

*Depending on the output for*
>nproc

12. Then install opencv using:

>sudo make install 

13. Then add the opencv configuration to the ubuntu ldconfig using:

>sudo sh -c 'echo "/usr/local/lib" >> /etc/ld.so.conf.d/opencv.conf'

>sudo ldconfig

