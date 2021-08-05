#ubuntu

best link : https://discuss.ardupilot.org/t/how-to-cross-compile-qgroundcontrol-for-raspberry-pi3/26790/41


sudo apt install libgles2-mesa-devqtquickcontrols2-5-dev


sudo apt-get install speech-dispatcher libudev-dev libsdl2-dev 


sudo apt-get install libqt5svg5-dev  


sudo apt install qtlocation5-dev qtpositioning5-dev
 
sudo apt-get install -y libqt5texttospeech5-dev

sudo apt install qtspeech5-speechd-plugin

sudo apt install -y qtmultimedia5-dev   


sudo apt-get install libqt5serialport5-dev

sudo apt qtbase5-private-dev

sudo apt-get install libudev-dev libinput-dev libts-dev libxcb-xinerama0-dev libxcb-xinerama0


sudo apt-get install speech-dispatcher libudev-dev libsdl2-dev libgstreamer1.0-0 gstreamer1.0-plugins-base libgstreamer-plugins-base1.0-dev


sudo apt install qt5-default qtbase5-private-dev qtbase5-dev qtbase5-dev-tools libqt5texttospeech5-dev libqt5svg5-dev qtmultimedia5-dev libqt5serialbus5-dev libqt5charts5-dev libqt5serialport5-dev qtdeclarative5-private-dev qttools5-private-dev qtquickcontrols2-5-dev libssl-dev




You need to build QtLocation from sources, because QGC requires location-private and positioning-private which is not available into repos:
git clone https://github.com/qt/qtlocation.git
cd qtlocation
git checkout v5.11.3
mkdir build
cd build/
qmake ../qtlocation.pro
make -j4
sudo make install


sudo apt install libqt5waylandclient5-dev 



