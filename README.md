# DrivePX2
Steps to flash TEGRA of Drive PX 2 and install ROS 

Note: This is a step by step method of the instructions given on developers.nvidia.com to make it easier for an average user to flash the TEGRA A/B. Incase of any discrepancies visit partners.nvidia.com and refer to the documentation. 

Pre requisites: 
A Ubuntu computer running either Ubuntu 16.04 or 14.04 (as on Sep 14th 2018) 
A USB to USB cable to connect your host machine and NVIDIA Drive px 2 
Internet connection on the host computer as well as on the Drive PX 2(need a ethernet cable) 
Please go through the getting started manual incase of any confusion 
 
-Visit https://developer.nvidia.com/drive-archive, create an account with Nvidia and make sure to use your university/company registered mail id (to get access to the Drive sub topic) 
-Download the Driveinstall from site. I tried the NVIDIA DRIVE 5.0.5.0a (February 12, 2018) and  NVIDIA DRIVE 4.1.8.0 (July 31, 2017). I was facing a few issuees with ROS on 5.0.9.0a (as on October 01, 2018). I would recomment to use 4.1.8.0 version. 

-Follow the instructions from https://docs.nvidia.com/drive/driveinstall_docs/#developertools/mobile/driveinstall/linux/5.0.5.0b/sdk/install.htm%3FTocPath%3D_____3 

-The rest of the process is well documented in the above link. The installer will download all the required software and install everything on the drive PX 2. The GUI will also have prompts to all the processes happening. 
-The Monitor connected to the Drive PX2 will go blank when the Tegra is being flashed. It should resume normal operation once it gets flashed and new OS has been loaded. 
-There will be prompt asking if the system needs to be password protiected. Based on your convenience you can opt for any of them. 
-Incase you choose for a password validation, the usernames and password are created. 
 
Username:  nvidia 
Default Password :  nvidia 
 
Username: ubuntu 
Default Password : ubuntu 

To install ROS on the drive px 2  follow the instructions from https://devtalk.nvidia.com/default/topic/1032204/faq/drive-px2-ros-installation/ till step 8. Refrain from step 4 if its your first time. I wasn't able to open the terminal after reboot when I tried step 4. 

After that 
initialise rosdep
-sudo rosdep init
-rosdep update
Environment setup
-echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
-source ~/.bashrc
 optional 
-sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential

Once ROS is installed follow the steps at http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment to setup your ROS environment

