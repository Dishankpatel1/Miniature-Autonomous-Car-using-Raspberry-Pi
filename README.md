# Miniature-Autonomous-Car-using-Raspberry-Pi
The project outcome is a miniature autonomous car for the exploration and navigation of the environment equipped with an HC-SR04 sensor to avoid unnecessary obstacles and a Pi-camera module to recognise object.

Before starting the project, ensure you are running the latest version of python, numpy and necessary libraries under rasbian software. 

~$ sudo apt update

~$ sudo apt dist-upgrade

~$ sudo apt autoclean

~$ sudo reboot

Additionally ensure latest version of OpenCV is installed. Below shows the list of commands implemented to install or update to the latest version of OpenCV. Note, follow all the steps in order or if updating to future version change the number version number respectively mentioned in line 9, 10 and 14.

1.	sudo apt-get update && sudo apt-get upgrade && sudo rpi-update
2.	sudo nano /etc/dphys-swapfile 
CONF_SWAPSIZE=2048
3.	sudo apt-get install build-essential cmake pkg-config
4.	sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev
5.	sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
6.	sudo apt-get install libxvidcore-dev libx264-dev
7.	sudo apt-get install libgtk2.0-dev libgtk-3-dev
8.	sudo apt-get install libatlas-base-dev gfortran
9.	wget -O opencv.zip https://github.com/opencv/opencv/archive/4.1.0.zip
10.	wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/4.1.0.zip
11.	unzip opencv.zip
12.	unzip opencv_contrib.zip
13.	sudo pip3 install numpy
14.	cd ~/opencv-4.1.0/
15.	mkdir build
16.	cd build
17.	cmake -D CMAKE_BUILD_TYPE=RELEASE \
-D CMAKE_INSTALL_PREFIX=/usr/local \
-D INSTALL_PYTHON_EXAMPLES=ON \
-D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib-4.1.0/modules \
 -D BUILD_EXAMPLES=ON ..
18.	make -j4
19.	sudo make install && sudo ldconfig
20.	sudo reboot


# The breakdown of project stages are listed below :

# Components Required 
The project initiates with finding of essential components required and creating a bill of materials/components for ordering. (Note : All generic components such as jumper-wires, LEDs, screws, copper stand-off and others are not mentioned as it can be obtained externally)
![BIll of Components](https://user-images.githubusercontent.com/100168764/168693849-db7f2071-b8d6-4ef0-8321-943c269cd5ff.jpg)


# Designing Parts 
Please refer to Porgramming & Testing folder. Alternatively, access all the step file parts of the car via below link: 
https://drive.google.com/drive/folders/1RpqP54dAROcASdLiJPIBShN6cyHpaFWD?usp=sharing 


# Aseembling Robot 
Once all parts are manufactured please install the car accordingly to the steps shown in the Final Report 6.4 Assembling the robot section. (Note: if the report is not available/viable please contact me, as this could be due to incompetence of report marking causing plagiarism)

Use necessary components to assemble the car, such as screw, nylon spacer, copper stand-off, etc.


# Hardware Connection
Below shows the connection diagram created using Fritzing software with the understanding of GPIO-pins from the datasheet of Raspberry-Pi 4B. Note, additional mini-breadboard is used to create a common +5V and GND line, due to only two +5V rail availability on Raspberry-Pi GPIO-pins

![Connection Diagram V1](https://user-images.githubusercontent.com/100168764/168692178-78408471-d456-4aa8-9913-b72c7e377bc6.jpg)

# Programming & Testing 

Please refer to Porgramming & Testing folder, where sub-modules codes are created testing individual hardware which contructs the final code

Additionally, project test videos are created showing all step-by-step approach displaying the build process of final code.

To access all videos link on the below link :
https://drive.google.com/drive/folders/1_9hdZoA_hv87OM3LIBfKxPX3ET0azrTL?usp=sharing 

Alternatively, the scan QR shown below using your phone:

![QR code for Videos](https://user-images.githubusercontent.com/100168764/168691425-b1d91318-60fc-4dc8-8047-24cf7a5cc1f4.png)
