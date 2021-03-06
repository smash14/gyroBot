# GyroRobot
<b>UPDATE: Code not working with iOS 12.2:</b> https://www.redmondpie.com/ios-12.2-will-prevent-motion-orientation-access-in-safari-unless-enabled/

Use the ESP-12E WiFi module and the gyro sensor of your smartphone to control a robot


## Components used in this in this project:
- ESP-12E on NodeMCU 1.0
- H bridge L298N
- 2x DC motors

## Arduino IDE settings:
- Add ESP boards via Preferences / Settings and add the following url into the Additional Board Manager URLs:  http://arduino.esp8266.com/stable/package_esp8266com_index.json
- Add ESPAsyncWebServer library: https://github.com/me-no-dev/ESPAsyncWebServer
- Add ESPAsyncTCP library: https://github.com/me-no-dev/ESPAsyncTCP
- Install the Arduino ESP8266 filesystem uploader to make use of SPIFFS filesystem (https://github.com/esp8266/arduino-esp8266fs-plugin)
    - This plugin allows you to upload html files directly to the ESP
    - All files stored in the data subfolder of your Arduino sketch path will be uploaded   
- Board Settings:
    - Board: "NodeMCU 1.0 (ESP-12E Module)"
    - Flash Size: "4M (1M SPIFFS)"

## Wiring

L298N | ESP2866
------|-------------
enA   | D1  (GPIO5)
in1   | D2  (GPIO4)
in2   | D5  (GPIO14)
in3   | D6  (GPIO12)
in4   | D7  (GPIO13)
enB   |D8  (GPIO15)

## Usage

- Upload the Arduino Sketch File with the recommended board settings.
- Upload the html file by cklicking on "Tools" --> "ESP8266 Sketch Data Upload"
- Connect to the Wifi network created by the ESP
- Open your webbrowser and go to 192.168.4.1
