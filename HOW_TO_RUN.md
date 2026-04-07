you can customize the operation and control through ADB or sh or taker. The following is an example based on ADB. The principle is that you do not need to directly install the complete apk. You can control the device through a certain DEX data package in the program. , the advantage is that it is perfect and completely DIY

The method only needs to extract the DEX in the installation package, and use ADB to implement the method of pretending to turn off the screen. You can directly run commands in NODE or HASS for control, or you can directly use other automation software to switch on and off in the device.

After downloading the file, upload the file to /storage/emulated/0/Download/, and then you can execute the command to run it, which basically solves the problem of turning off the screen.

adb -s ip:5555 shell CLASSPATH=/storage/emulated/0/Download/DisplayToggle.dex app_process / DisplayToggle 1 #Open the screen

adb -s ip:5555 shell CLASSPATH=/storage/emulated/0/Download/DisplayToggle.dex app_process / DisplayToggle 0 #Turn off the screen
