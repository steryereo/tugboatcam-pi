# tugboatcam-pi

## Resources:
- https://motion-project.github.io/motion_guide.html
- https://learn.adafruit.com/cloud-cam-connected-raspberry-pi-security-camera/dropbox-sync

## Installation
Install motion
```
sudo apt-get install motion
```
Config file
```
cp ./motion.conf /etc/motion/motion.conf # or wherever you have motion pointed
```

install and config aws-cli
```
sudo apt-get awscli
aws configure # this will put your config and credential files in ~/.aws

# make aws config files readable by all users
chmod a+r ~/.aws/config
chmod a+r ~/.aws/credentials
```

install upload script
```
chmod a+x uploadfile
sudo cp uploadfile /usr/local/bin/uploadfile
```

start it up!
```
sudo service motion start # I don't remember if you have  to do something to enable the service first
```
