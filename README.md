cadi-bt-mon
===========

Cadi Bluetooth remote monitor and control for Android

The application used to read the data from Cadi grow controller via Bluetooth SPP profile.
The source code of BlueTerm was used in this project.

v1.2
- Added pseudo CRC (XOR) for 64-byte data blocks.

v1.1
- Value/time diagrams to draw temperature, humidity, pH and EC levels

Software uses DeviceActivityList (from BlueTerm) for fetching the devices found by Android Bluetooth module and BluetoothSerialService to establish and keep connecton. On the controller side there is a UART<->Bluetooth convertor (HC-04/HC-06 type), that sends current sensor and device data to Android device via Bluetooth. By default convertor works on 9600baud.
Data block consists of 63 bytes of load and 1 byte that equals to XOR function on sequence of the rest 63, so in total we have 64bytes fixed length blocks, that are being received by Android application.

visit http://plantalog.livejournal.com for more info on Cadi grow controller project
