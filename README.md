# Reproduction of ESP8266 SoftwareSerial compilation error

```sh
$ pio run
Processing d1_mini (platform: espressif8266; board: d1_mini; framework: arduino)
--------------------------------------------------------------------------------
Verbose mode can be enabled via `-v, --verbose` option
CONFIGURATION: https://docs.platformio.org/page/boards/espressif8266/d1_mini.html
PLATFORM: Espressif 8266 (2.7.4+9) > WeMos D1 R2 and mini
HARDWARE: ESP8266 80MHz, 80KB RAM, 4MB Flash
PACKAGES: 
 - framework-arduinoespressif8266 @ 2.7.4+9 
 - tool-esptoolpy @ 1.30301.220515 (3.3.1) 
 - toolchain-xtensa @ 2.40802.200502 (4.8.2)
LDF: Library Dependency Finder -> https://bit.ly/configure-pio-ldf
LDF Modes: Finder ~ chain, Compatibility ~ soft
Found 29 compatible libraries
Scanning dependencies...
Dependency Graph
|-- EspSoftwareSerial @ 6.10.0
Building in release mode
Compiling .pio/build/d1_mini/src/main.cpp.o
Compiling .pio/build/d1_mini/libab3/SoftwareSerial/SoftwareSerial.cpp.o
In file included from .platformio/packages/framework-arduinoespressif8266/libraries/SoftwareSerial/src/SoftwareSerial.cpp:23:0:
.platformio/packages/framework-arduinoespressif8266/libraries/SoftwareSerial/src/SoftwareSerial.h:132:9: error: 'int SoftwareSerial::availableForWrite()' marked override, but does not override
     int availableForWrite() override {
         ^
In file included from src/main.cpp:2:0:
.platformio/packages/framework-arduinoespressif8266/libraries/SoftwareSerial/src/SoftwareSerial.h:132:9: error: 'int SoftwareSerial::availableForWrite()' marked override, but does not override
     int availableForWrite() override {
         ^
*** [.pio/build/d1_mini/src/main.cpp.o] Error 1
*** [.pio/build/d1_mini/libab3/SoftwareSerial/SoftwareSerial.cpp.o] Error 1
========================= [FAILED] Took 0.32 seconds ===========================
```