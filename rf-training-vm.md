# Installing clean VM for training Robotframework

## Creating the Ubuntu VM
In Hyper-V Manager create a new VM
* Quick Create ... 
* Choose Unbuntu 18 or so (doesnt really matter)
* When everything has booted run the following commands or create a script for it (might do that later)

## Updating package list
```
sudo apt-get update
```

## Installing Python3
```
#sudo apt-get install python3 # (apparently already installed on image from MS)
sudo apt-get install -y python3-pip
sudo python3 -m pip install --upgrade pip
```

## Installing robotframework and libraries
```
pip install robotframework
pip install robotframework-seleniumlibrary
pip install robotframework-datadriver
```

## Install chrome
```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
```

## install chromedriver
```
wget -N https://chromedriver.storage.googleapis.com/81.0.4044.69/chromedriver_linux64.zip
unzip chromedriver_linux64.zip
chmod +x chromedriver

sudo mv -f chromedriver /usr/local/share/chromedriver
sudo ln -s /usr/local/share/chromedriver /usr/local/bin/chromedriver
sudo ln -s /usr/local/share/chromedriver /usr/bin/chromedriver
```

# run selenium headless | !!! Voor Trainingen niet nodig !!!
# sudo apt-get install xvfb

## Install pycharm
```
sudo snap install pycharm-community --classic
```

Manual steps in Pycharm after installing
* Installing Intellibot plugin for autocomplete
 * File > Settings > Plugins > search for: Intellibot
