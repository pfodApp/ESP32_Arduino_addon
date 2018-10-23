# ESP32_Arduino_addon
Snapshot of https://github.com/espressif/arduino-esp32 and https://github.com/nkolban/ESP32_BLE_Arduino used by pfodDesigner
The copyright for those files are as specified in their respective githubs

Note: this repository is out-of-date and GitHub will not accept the update (file >25Mb)
Download zip from www.forward.com.au/pfod/ESP32/ESP32_hardware.zip

# Installing the Arduino Support for the ESP32
As at April 2018, installing the Arduino ESP32 support is more involved then for most other boards and the code libraries supplied are not complete. You cannot use the Arduino Board manager to install the ESP32 support. Follow these steps to setup Arduino for ESP32 programming

Find the path of your Arduino Sketchbook location Directory. Open Arduino IDE and look under File->Preferences and at the top of that screen you will see the Sketchbook location.

Download this ESP32_hardware.zip file and unzip it to the Sketchbook location. It creates a hardware sub-directory there. In the unlikely event you already have a hardware sub-directory in your Sketchbook location, merge its contents with this one.

Install the Xtensa and ESP32 Tools. Go to the hardware\espressif\esp32\tools directory then
For Windows machines run the get.exe file. 
For Mac and Linux users should run the get.py python script to download the tools. Using a terminal, navigate to the hardware/espressif/esp32/tools folder. 
Then type: python get.py
The “get.py” python script will download the Xtensa GNU tools and the ESP32 software development kit (SDK), and unzip them to the proper location. 
You should see a few new folders in the “tools” directory, including “sdk” and “xtensa-esp32 -elf” once it’s done.
Note: This download and install takes some time to process the ~0.5Gig of files.

Once this is complete, close and re-open your Arduino IDE and you should now have a long list of ESP32 boards to choose from under the Tool->Boards menu. 
Choose “SparkFun ESP32 Thing”

You can then open the File-Examples list to see a number of ESP32 example files.

The process above install as snapshot of the github code for the ESP32 and BLE support. The pfodDesigner generated code and the examples below use this version of those libraries. If you want the latest version, with possibly a different set of features and bugs, then download the zip of the latest version of the https://github.com/espressif/arduino-esp32 and unzip it to hardware/espressif and rename the folder esp32 and then for the BLE support download a zip of the latest version of the https://github.com/nkolban/ESP32_BLE_Arduino and unzip it to the esp32/libraries folder and rename it ESP32_BLE_Arduino (if necessary).
