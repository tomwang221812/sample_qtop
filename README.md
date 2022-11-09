# sample_qtop
A sample tool to monitor system through adb

# Requriment
  - Ubuntu Host
  - Hexagon SDK 4.5.0.3 under `$HOME/Qualcomm/Hexagon_SDK`
  - Android debug bridge (ADB) `sudo apt install adb`

# Install and Run
1. Clone this repo
2. cd sample_qtop
3. Download the `simple_curses.sh` from [here](https://github.com/metal3d/bashsimplecurses)
4. sudo chmod a+x sample_qtop_adb
5. Connect your device through usb and tcpip to run => ./sample_qtop_adb

# Connect ADB through tcpip
`
adb devices # Check connected device serial
adb -s ${YOUR_DEVICE_SERIAL} wait-for-device tcpip 5555
adb -s ${YOUR_DEVICE_SERIAL} wait-for-device root
adb connect ${DEVICE_IP}:5555
adb -s ${DEVICE_IP}:5555 shell echo 'Hello World!'
`
