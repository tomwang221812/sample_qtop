# sample_qtop
A sample tool to monitor RB5 and RB6 device with Linux Ubuntu Opertaing system through adb

# Preview
![](https://github.com/tomwang221812/sample_qtop/blob/main/preview.png)

# Feature
[ ] TODO

# Requriment
  - Ubuntu Host
  - Hexagon SDK 4.5.0.3 under `$HOME/Qualcomm/Hexagon_SDK`
    - sysMonAppLE_64bit must be pushed to device under `/data/sysMonApp`
    - mini-dm 1.0
  - Android debug bridge (ADB) `sudo apt install adb`
  - [Bash Simple Curses](https://github.com/metal3d/bashsimplecurse) script `simple_curses.sh`

# Install and Run
1. Clone this repo
2. cd sample_qtop
3. Download and copy the `simple_curses.sh` to the same directory
4. sudo chmod a+x sample_qtop_adb
5. Connect your device through usb and tcpip to run => `./sample_qtop_adb`

# Connect ADB through tcpip
```
adb devices # Check connected device serial
adb -s ${YOUR_DEVICE_SERIAL} wait-for-device tcpip 5555
adb -s ${YOUR_DEVICE_SERIAL} wait-for-device root
adb connect ${DEVICE_IP}:5555
adb -s ${DEVICE_IP}:5555 shell echo 'Hello World!'
```
