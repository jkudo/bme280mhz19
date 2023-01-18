# BME280 と MH-Z19B
BME280 と MH-Z19B からデータを収集します。
- 気温
- 気圧
- 湿度
- 二酸化炭素濃度

## Serial Portの設定
```
# raspi-config
```
```
3 Interface Options
P6 Serial Port

Would you like a login shell to be accessible over serial? -> No
Would you like the serial port hardware to be enabled? -> Yes

再起動
```
```
pip install mh-z19
```

## I2Cの設定
```
# raspi-config
```
```
3 Interface Options
P5 I2C

Would you like the ARM I2C interface to be enabled? -> Yes

一応再起動
```

## 実行
```
# python sample.py
```
```
気温           :  28.1 C
気圧           :  1016.71760299 hPa
湿度           :  30.0947604882 %
二酸化炭素濃度 :  980 ppm
```

# BME280 and MH-Z19B
Data collect from BME280 and MH-Z19B

Original
https://www.raspberrypi-spy.co.uk/2016/07/using-bme280-i2c-temperature-pressure-sensor-in-python/
