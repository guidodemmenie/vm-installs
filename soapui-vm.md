# Installing clean VM for SoapUI
## Creating the Ubuntu VM
In Hyper-V Manager create a new VM
* Quick Create ... 
* Choose Unbuntu 18 or so (doesnt really matter)
* When everything has booted run the following commands or create a script for it (might do that later)

## Updating package list
```
sudo apt-get update
```

## Installing Java JRE
```
sudo apt-get install -y openjdk-8-jre-headless
```
Getting an older one because SoapUI should work better on this one.

## Installing SoapUI
```
wget https://s3.amazonaws.com/downloads.eviware/soapuios/5.5.0/SoapUI-5.5.0-linux-bin.tar.gz
tar -xzf SoapUI-5.5.0-linux-bin.tar.gz -C /opt/
cd /opt/SoapUI-5.5.0/bin/
./soapui.sh
```
