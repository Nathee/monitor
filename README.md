# BrewBench

<img src="img/brewbench-logo.png?raw=true" alt="BrewBench logo" title="BrewBench" align="right" />

[![Stories in Ready](https://badge.waffle.io/BrewBench/web-controller.png?label=ready&title=Ready)](https://waffle.io/BrewBench/web-controller)

BrewBench is an Arduino brew monitor, controller and alert system for the home brewer enthusiast.  It uses the Arduino REST API to interface with thermistors connected to the analog ports.  You can also connect a relay to the digital ports and add a heater / pump to create a RIMS system.  The software will start/stop the heater/pump based on the target temperature you set.

## Setup the Arduino

* Wire up the temp Sensors
  * Analog [Thermistors](https://learn.adafruit.com/thermistor/using-a-thermistor)
  * Digital [DS18B20](https://www.adafruit.com/product/381)
    * Will need the [cactus](http://static.cactus.io/downloads/library/ds18b20/cactus_io_DS18B20.zip) library

## Arduino Board Options

Power up and connect to the default IP http://192.168.240.1/

### Yun Arduino.cc setup
  * If the WiFi network starts with Arduino use password: arduino
  * Set REST API access to open
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

## Open BrewBench

Go to [brewbench.io](http://brewbench.io) or clone this repo and start the webserver and go to [http://127.0.0.1:8080](http://127.0.0.1:8080).

```sh
npm install
live-server
```

## Development

For development just run `npm install`, and look at [index.html](index.html) for un-commenting the un-minified files.

```sh
npm install
gulp
```

<img src="img/screenshot-desktop.png?raw=true" alt="BrewBench screenshot" align="center" />

<img src="img/brewbench-wiredup.jpg?raw=true" alt="BrewBench wired up" align="center" />

## Thanks

* For the Lovibond Hex colors: http://brookstonbeerbulletin.com/thinking-about-beer-color
* For the SVG icons:
  * https://thenounproject.com/dejv
  * https://thenounproject.com/creativestall
* For the Hop and Grain reference: https://byo.com
* For the recipes: http://beersmithrecipes.com
* For the bell sounds: http://www.orangefreesounds.com/category/sound-effects/bell-sound

## About

[BrewBench](//brewbench.co) is a brew monitor and controller Developed by [Andrew Van Tassel](//www.andrewvantassel.com) and [Lee Kendrick](http://www.leekendrick.info) &copy;2016.

Made with <img src="img/beer.png" width="45"> from Colorado
