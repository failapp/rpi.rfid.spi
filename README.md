### rpi.rfid.spi
raspberry pi 3 - lector rfid - protocolo spi - libreria bcm2835

linux ubuntu server 20.04
```
wget http://www.airspayce.com/mikem/bcm2835/bcm2835-1.68.tar.gz
tar -zxf bcm2835-1.68.tar.gz
cd bcm2835-1.68
./configure
sudo make check
sudo make install
```

compilación de proyecto c++:
```
g++ MFRC522.cpp Read.cpp -std=c++11 -lbcm2835
```

### Pin layout
The following table shows the pin layout used:

+-----------+----------+-------------+
|           | MFRC522  | Raspberry Pi|
+-----------+----------+-------------+
| Signal    | Pin      | Pin         |
+===========+==========+=============+
| RST/Reset | RST      | 22          |
+-----------+----------+-------------+
| SPI SS    | SDA      | 24          |
+-----------+----------+-------------+
| SPI MOSI  | MOSI     | 19          |
+-----------+----------+-------------+
| SPI MISO  | MISO     | 21          |
+-----------+----------+-------------+
| SPI SCK   | SCK      | 23          |
+-----------+----------+-------------+
| 3V        | 3v       | 1           |
+-----------+----------+-------------+
| GND       | GND      | 25          |
+-----------+----------+-------------+


libreria bcm2835
```
http://www.airspayce.com/mikem/bcm2835/index.html
```