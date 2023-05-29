<h1 align="center"><img src="assets/Raspberry_Pi_Logo.svg" height="auto" width="40"></img> ObjectDetectionPI </h1>





***Detect Object using raspberry pi***

- [X] Cocodataset - Common Object Context
- [X] Raspberry PI
- [X] Opencv
- [X] Camera CSI
- [X] OS Ubuntu Server 22.04 LTS


##

**Requirements:**

```
sudo apt install raspi-config
```
⚠️ Enable CSI-CAM interface!!

```
sudo raspi-config
```
 * Interface
 * Enable Legacy Cam


Python default name:

```
sudo ln -sf /usr/bin/python3 /usr/bin/python
```
```
sudo apt install python3-pip -y
```
```
sudo apt-get install build-essential cmake pkg-config -y && sudo apt-get install libjpeg-dev libtiff5-dev -y && sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev -y && sudo apt-get install libxvidcore-dev libx264-dev -y && sudo apt-get install libgtk2.0-dev libgtk-3-dev -y && sudo apt-get install libatlas-base-dev gfortran -y && sudo pip install numpy
```

```
sudo apt update && sudo apt upgrade
```

Check Cam:

Install:

```
sudo apt install v4l-utils -y
```
Check:
```
v4l2-ctl --list-devices
```
Return:
* `v4l2-ctl --list-devices`
    - [x] CSI CAM: `/dev/video0`

OpenCv Install:

```
sudo apt-get update
sudo apt install libopencv-dev python3-opencv
sudo nano /boot/firmware/config.txt
```
add last line: `start_x=1`



```
sudo apt-get update
sudo apt-get upgrade
sudo reboot
```

##


 Detect object

```
python detect1.py
```
```
python detect2.py
```
##

Face Detect

```
pip install face-recognition 
pip install imutils
```

```
sudo nano /etc/dphys-swapfile
```

Update value `CONF_SWAPSIZE = 2048`

New value:
```
CONF_SWAPSIZE = 100
```
Restart 
```
sudo systemctl restart dphys-swapfile
```
