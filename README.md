# Iot-Based-Patient-Health-Monitoring-System-Using-ESP-32-Web-Server
IoT-based healthcare system using ESP32 integrates MAX30100, DS18B20, and DHT11 sensors for real-time health monitoring. It provides analytics for remote management and early detection of health issues, ensuring accurate, continuous data tracking and enhanced patient care.

Components and Its details


1. MAX30100 Pulse Oximeter Sensor

The sensor is an integrated pulse oximetry and heart-rate monitoring solution. It features two LEDs, a photodetector, optimized optics, and low-noise analog signal processing to accurately detect pulse and heart-rate signals. It operates with 1.8V and 3.3V power supplies and includes a software-controlled power-down mode, allowing the power supply to stay connected with minimal standby current.

<img decoding="async" src="https://how2electronics.com/wp-content/uploads/2019/06/MAX30100-300x300.jpg" alt="MAX30100 Pulse Oximeter Sensor" width="200" height="200" class="aligncenter size-thumbnail wp-image-2254" srcset="https://how2electronics.com/wp-content/uploads/2019/06/MAX30100-300x300.jpg 300w, https://how2electronics.com/wp-content/uploads/2019/06/MAX30100-150x150.jpg 150w, https://how2electronics.com/wp-content/uploads/2019/06/MAX30100.jpg 600w" sizes="(max-width: 200px) 100vw, 200px" />



2.DS18B20 Temperature Sensor


This is a pre-wired and waterproofed version of the DS18B20 sensor. Handy for when you need to measure something far away, or in wet conditions. The Sensor can measure the temperature between -55 to 125°C (-67°F to +257°F). The cable is jacketed in PVC.

![waterproof-temperature-sensor-ds18b20-300x249](https://github.com/user-attachments/assets/6d3da236-52c4-49a2-ab22-27ec5fbbbd5b)


3.DHT11 Humidity & Temperature Sensor


The DHT11 is a basic, ultra low-cost digital temperature and humidity sensor. It uses a capacitive humidity sensor and a thermistor to measure the surrounding air, and spits out a digital signal on the data pin (no analog input pins needed).

![DHT11-Humidity-Temperature-Sensor-360x360](https://github.com/user-attachments/assets/aebf4ee4-8beb-4bdf-be2b-8376dc8303b5)


CIRCUIT DIAGRAM:

So the circuit digram for interfacing MAX30100, DHT11 & DS18B20 with ESP32 is given below.

All the sensors operate on a 3.3V VCC. Connect their VCC to a 3.3V power supply and their GND to GND.




The MAX30100, an I2C sensor, requires:


SDA connected to GPIO21.
SCL connected to GPIO22.
INT connected to GPIO19 of the ESP32.




The DHT11 sensor has its output pin connected to GPIO18 of the ESP32.




The DS18B20 sensor connects as follows:


Output pin connected to GPIO5 of the ESP32.
A 4.7K pull-up resistor connected between its output pin and VCC.




![Iot-Based-Patient-Health-Monitoring-System-ESP32-1](https://github.com/user-attachments/assets/c518a805-b09b-4e9e-a5e5-9447bee84d27)


Here I assembled the circuit on a breadboard.


![MAX30100-DS18B20-DHT11](https://github.com/user-attachments/assets/a47a074e-bb73-4eb9-abc0-11dde037ffd7)

Results & Working of the Project:

After uploading the code, open the serial monitor. The ESP32 will attempt to connect to the network. Once successfully connected, it will display the IP address.
![1-1-528x540](https://github.com/user-attachments/assets/cffab865-3500-400b-9b90-7152be8fe928)

Copy the IP Address, paste it into any web browser, and press Enter. This will display details such as room temperature, room humidity, heart rate, blood oxygen level, body temperature, and more.

![s1-960x455](https://github.com/user-attachments/assets/49359c9b-5a1c-43a5-8f1b-22e6bed26fac)
 
