
[![Arduino CI](https://github.com/RobTillaart/DHTINT/workflows/Arduino%20CI/badge.svg)](https://github.com/marketplace/actions/arduino_ci)
[![Arduino-lint](https://github.com/RobTillaart/DHTINT/actions/workflows/arduino-lint.yml/badge.svg)](https://github.com/RobTillaart/DHTINT/actions/workflows/arduino-lint.yml)
[![JSON check](https://github.com/RobTillaart/DHTINT/actions/workflows/jsoncheck.yml/badge.svg)](https://github.com/RobTillaart/DHTINT/actions/workflows/jsoncheck.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/RobTillaart/DHTINT/blob/master/LICENSE)
[![GitHub release](https://img.shields.io/github/release/RobTillaart/DHTINT.svg?maxAge=3600)](https://github.com/RobTillaart/DHTINT/releases)


# DHTINT

Arduino library for DHT sensors - integer only


## Description

This is an **experimental** integer only version of the DHTNEW library.

As it uses only integers only to reduce footprint, so it becomes more 
usable for the very small processors like the ATTINY 45 or 85. 

As the library only uses integers it will not trigger the including of 
the floating point math libraries, saving additional memory.

Relates to - https://github.com/RobTillaart/DHTNew


### Compare DHTINT versus DHTNEW

Sketch: ..\example\dhtint_minimum.ino

replaced DHTINT with DHTNEW


| platform | library | sketch size | variables |
|:--------:|:--------|------------:|----------:|
|  UNO     | DHTNEW  |        5730 |       341 |
|  UNO     | DHTINT  |        3978 |       321 |
|          | delta   |        1752 |        20 |
|          |         |             |           |
|  ESP32   | DHTNEW  |      206730 |     13464 |
|  ESP32   | DHTINT  |      206110 |     13456 |
|          | delta   |         620 |         8 |
|          |         |             |           |


Gain is most substantial for the UNO platform.


## Future

- Keep in sync with DHTNEW.
- Test more
- Add examples.

