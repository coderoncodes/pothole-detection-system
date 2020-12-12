# pothole-detection-system
Complete steps to a working pothole detection system. 
Preparing Python
Uninstall “python” and “python launcher” from the Control Panel. (If you have python installed beforehand.)
Download miniconda and install https://docs.conda.io/en/latest/miniconda.html

When asked, click that check box.(add anaconda to my PATH…)

Installing CUDA Libraries
Head over to this site, download and install the cuda toolkit
https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exelocal
the config:

Download cudnn from drive
Extract it and copy the “cuda” folder.
Create new folder in C:\ with name “tools” and paste inside it
Go to desktop ,Right click “this pc” 
Properties=> Advanced System Settings=> Environment variables
Scroll down and double click “Path”

Click new button
Paste “C:\tools\cuda\bin” click ok and close it
Setting up the Project Files 
Download and Extract the rar file.
Inside the directory, open a python file named predict.
In main function check for the place where it denotes image path and change the image name in that place or change the name of the image in directory.
Save that python file and exit.
Copy the directory path.
Example:

Get back to cmd and execute the following stuff one by one
cd “directory u copied”
Or just go to the directory and type cmd in the address bar.
Installing required modules
Open command prompt with admin privileges
Execute upcoming commands one by one
conda create --name tf-gpu

(press y and enter) 
conda activate tf-gpu
Installing tensorflow:
conda install tensorflow-gpu
(press y and enter)
To verify tensorflow installation type:
python
Type the code 
import tensorflow as tf
print(tf.__version__)
Installing Keras:
conda install keras
(press y and enter)
Installing Opencv:
conda install opencv
(press y and enter)
Installing Imgaug:
conda config --add channels conda-forge
conda install imgaug
(press y and enter)
conda install tqdm
(press y and enter)
python predict.py
wait for it to complete and check the directory
To Exit console press ctrl+Z

