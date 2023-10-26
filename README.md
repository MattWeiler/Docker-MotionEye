# Docker-MotionEye

https://github.com/ccrisan/motioneye



**MotionEye Docker** is a surveillance solution base on: _MotionEye_, _Motion_ and _Docker_.

It's easy and ready to use. \
Just configure a camera and run this docker, then videos and images can be saved once a motion is detected while a notification e-mail including the recorded video and a preview image will be sent. \
On top of that, the webcam can be accessed anytime via HTTP live streaming.

# Default ADMIN Credentials
Username: admin
Password: 

***
# Host Paths -> Container Paths
## Configuration Path
/etc/motioneye -> /mnt/user/appdata/motioneye/config 
The path to where the MotionEye configuration will be stored.

## Media Files Path
/var/lib/motioneye -> /mnt/user/appdata/surveillanceVideos 
The path on your host system where the captured videos/images will be stored.

## Local Time Path
/etc/localtime -> /etc/localtime 
The path on your host system for the local-time. This will allow the MotionEye application to access the date/time from your host machine.


***
# Ports
## WEB UI
The port that you want to access your docker container from externally.

## Cam Streams
When adding cameras, you will have to define 1 port for each camera. 
This will be used to allow each camera stream to be accessible from outside the docker container. 
 
Simply add a port, with "connection type" of "TCP", for each camera. 
Ensure that each camera has a unique port and that for each camera, the "container port" and the "host port" are the same. 
 
In the MotionEye GUI, under the "Video Streaming" section for each camera, set the "Streaming Port" to match what you have setup as the "container port" when configuring the docker container.
