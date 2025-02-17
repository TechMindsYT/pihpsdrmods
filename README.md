# pihpsdrmods

This script is for installing PiHPsdr onto a RPi4 using a Radioberry. 

This first script (pihpsdr_install.sh) specifically changes the screen resolution to 1366 x 768 with NO SOAPY support.

The second script (pihpsdr_install_soapy.sh) is for use with a 800 x 480 screen and it also enables SOAPY support.

## Install the following first, if you want to use SOAPY.
```
sudo apt-get install -y git build-essential automake cmake

git clone https://github.com/pothosware/SoapySDR.git
cd SoapySDR
mkdir build
cd build
cmake ..
make
sudo make install
sudo ldconfig 

sudo apt-get install rtl-sdr librtlsdr-dev

git clone https://github.com/pothosware/SoapyRTLSDR.git
cd SoapyRTLSDR
mkdir build
cd build
cmake ..
make
sudo make install
sudo ldconfig 


git clone https://github.com/SDRplay/SoapySDRPlay
cd SoapySDRPlay
mkdir build
cd build
cmake ..
make
sudo make install
sudo ldconfig 

```
