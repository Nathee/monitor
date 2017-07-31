# BrewBench Monitor Arduino Sketches

## Setup the Arduino

* Wire up a temp Sensors (Three options)
  * [Thermistors](https://learn.adafruit.com/thermistor/using-a-thermistor) (Analog)
  * [PT100](https://www.adafruit.com/product/3290) (Analog)
  * [DS18B20](https://www.adafruit.com/product/381) (Digital)
    * Will need the [cactus](http://static.cactus.io/downloads/library/ds18b20/cactus_io_DS18B20.zip) library
* Wire up a relay for heat and pump controls
  * [Solid State Relay (SSR)](https://www.sparkfun.com/products/13015)
    * Arduino GRD -> Relay DC Negative
    * Arduino Digital (D3) PWM ~ Port -> Relay DC Positive
  * [Sainsmart 2 channel relay](http://www.sainsmart.com/arduino-pro-mini.html)
    * Arduino GND -> Relay GND
    * Arduino 5V -> Relay VCC
    * Arduino Vin -> Relay JD-VCC (no jumper needed)
    * Arduino Digital (D2) Port -> Relay IN1 (heater)
    * Arduino Digital (D4) Port -> Relay IN2 (pump)

## Arduino Board Options

1. Power up and connect to the default IP http://192.168.240.1
1. Set the digital pin or analog pin depending on which temp sensor you're using.
1. Press play, you can adjust the temp by sliding the temp knob.

### Yun Arduino.cc setup
  * If the WiFi network starts with Arduino use password: arduino
  * Set REST API access to openÂ
  * Change or remember the host name or IP address (you will need this later)
  * Save to reboot
  * Using the [Arduino IDE](https://www.arduino.cc/en/Main/Software) upload the [BrewBenchYun sketch](arduino/BrewBenchYun/BrewBenchYun.ino)

### Yun Arduino.org (aka. Linino) setup
  * If the WiFi network starts with Linino use password: doghunter
  * Set REST API access to open
  * Change or remember the board name or IP address (you will need this later)
  * Save to reboot
  * Using the [Arduino IDE](https://www.arduino.cc/en/Main/Software) upload the [BrewBenchYunLinino sketch](arduino/BrewBenchYunLinino/BrewBenchYunLinino.ino)

### Uno WiFi Arduino.cc setup
  * If the WiFi network starts with Arduino use password: arduino
  * Set REST API access to open
  * Change or remember the host name or IP address (you will need this later)
  * Save to restart
  * Using the [Arduino IDE](https://www.arduino.cc/en/Main/Software) upload the [BrewBenchUnoWiFi sketch](arduino/BrewBenchUnoWiFi/BrewBenchUnoWiFi.ino)