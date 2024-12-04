# LoRa APRS Digipeater for Waveshare RP2040 LoRa

## You can support this project to continue to grow:

[<img src="https://github.com/richonguzman/LoRa_APRS_Tracker/blob/main/images/github-sponsors.png">](https://github.com/sponsors/richonguzman)     [<img src="https://github.com/richonguzman/LoRa_APRS_Tracker/blob/main/images/paypalme.png">](http://paypal.me/richonguzman)


____________________________________________________

(Afiliated Links:)

for _Waveshare RP2040 LoRa_:
[Aliexpress](https://s.click.aliexpress.com/e/_DmGeyrn) , [Waveshare](https://www.waveshare.com/rp2040-lora.htm?sku=26543)

____________________________________________________


## Instructions:

## 0) Connect Waveshare RP2040 ribbon cable between RP2040-LoRa module and USB-C connector.

## 1) Prepare the Configuration info: you have to copy two strings into __Serial__ : (A) Digipeater Configuration and (B) LoRa Configuration. Prepare this two Strings before flashing the board.

A) On the first Reboot (as Digipeater won't find any configuration) you should enter the following:

callsign,digiMode,symbol,overlay,comment,latitude,longitude,sendBatteryTelemetry,beaconInternal,ultraEcoMode

example: AB1CDE-11,1,#,L,Waveshare_RP2040-Digipeater,0.0000000,0.0000000,15

- callsign              = replace with your Valid Ham Callsign (in UpperCase).
- digiMode              = 1 for repeating "WIDE1-1", 2 for "WIDE2-n"
- symbol                = # ("#" is recommended)
- overlay               = L ("L" is recommended)
- comment               = Waveshare_RP2040-Digipeater (don't use any *coma* in comment text)
- latitude              = in degrees and better to have 7 decimals
- longitude             = in degrees and better to have 7 decimals
- beaconInterval        = 15 (minutes)

B) Prepare LoRa Configuration info:

Frequency,SpreadingFactor,SignalBandwidth,CodingRate4,Power

example: 433.775,12,125.0,5,22

- Frequency       = your QRG for LoRa APRS as per your Country Settings
- SpreadingFactor = 7 to 12 as per your Country Settings
- SignalBandwidth = 125.0 is stardard for all countries.
- CodingRate4     = 5 to 7 as per your Country Settings
- Power           = 22 (dBm) is max for SX1262 in Rak 4631 Module


## 2) Press and keep pressing BOOT button. Press RESET button and release RESET button. Now release BOOT button ("RPI-RP2" external disc should appear in your PC/MAC/Linux Desktop).

## 3) Drag "firmware_Waveshare_RP2040_Digipeater.uf2" file into the folder/external disk "RPI-RP2". It should reboot right away and you should get into any app that let you enter __Serial__ commands (Arduino IDE, VSCODE ...)

## 4) The initial setup will ask you to paste the string sentences created in __(A)__ first and then on another line __(B)__.

## 5) Follow the instructions on __Serial__ info to finish configuration.

## 6) After the sucess in writing configuration , the station will reboot and start right away.

   
if you want to delete previous configuration , drag "RP2040_DeleteConfig.uf2" into the folder/virtual disk when boards is in boot loader mode.

- 2024.11.04 First Test Firmware.

___________________________________________________

# Hope You Enjoy this, 73! CA2RXU, Valparaiso, Chile
