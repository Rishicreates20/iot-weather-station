# iot-weather-station

Arduino Project: Temperature and Humidity monitor Tutorial using DHT11 (or DHT22) sensor and LCD shield.
The main ingredient/ parts that will be used in this tutorial is the DHT11 temperature and humidity sensor. The sensor is capable of measuring the ambient temperature and humidity in a particular area. The DHT11 is a basic, ultra low-cost digital temperature and humidity sensor. It uses a capacitive humidity sensor and a thermistor to measure the surrounding air and spits out a digital signal on the data pin (no analog input pins needed). Its fairly simple to use, but requires careful timing to grab data. The only real downside of this sensor is you can only get new data from it once every 2 seconds.

some of the features of the sensor are listed below;

Low cost
3 to 5V power and I/O
2.5mA max current use during conversion (while requesting data)
Good for 20-80% humidity readings with 5% accuracy
Good for 0-50°C temperature readings ±2°C accuracy
No more than 1 Hz sampling rate (once every second)

Required Parts
1.Arduino Mega: https://educ8s.tv/part/ArduinoMega
2.Keypad display: https://educ8s.tv/part/KeypadShield
3.The DHT11 sensor: https://educ8s.tv/part/DHT11
4.OLED Multimeter: https://educ8s.tv/part/UsbDoctorOLED
5.Powerbank: https://educ8s.tv/part/Powerbank
6.Wires: https://educ8s.tv/part/Wires

Schematics
The schematics for this project is simple we only need to connect the DHT11 temperature andumidity sensor as shown in the schematics below.

<img width="496" alt="image" src="https://github.com/user-attachments/assets/4c11c5f8-5eb2-4df9-a1e4-1e0408b8643d" />
The 16×2 LCD display comes in form of a shield which makes it easy to mount the display on the Arduino.

Code
The code for this project is quite simple, as I will show you, it takes just 47 lines of code including comments and declarations to get the project working.

The algorithm behind the code for the project is quite simple, we start by establishing communications with the sensor after which we request for temperature and humidity readings from it. These readings are obtained in Celsius and Fahrenheit and are displayed on the 16×2 LCD display shield.

We will be using two libraries for this project, the DHT.h library to easily communicate with the DHT11 and the liquidcrystal.h library to make communication with the 16×2 LCD Display shield easy. while the liquidcrystal.h library comes pre-built with the Arduino, the DHT library does not, but it can be downloaded and installed from this link (https://github.com/adafruit/DHT-sensor-library)
