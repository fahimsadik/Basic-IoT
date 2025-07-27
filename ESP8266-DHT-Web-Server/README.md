# ESP8266 DHT Web Server
This project uses an ESP8266 microcontroller to read temperature and humidity data from a DHT11 sensor and serve it on a local web page. The web page automatically updates with the latest sensor readings.

# Components Needed
ESP8266 board (e.g., NodeMCU)

DHT11 Temperature and Humidity Sensor 


Jumper wires

Breadboard

# Circuit Connections
DHT11 Sensor Data pin -> ESP8266 Digital Pin 5 (

D1) 


DHT11 Sensor VCC -> ESP8266 3.3V or 5V

DHT11 Sensor GND -> ESP8266 GND

A 10K pull-up resistor from the data pin to VCC is recommended.

# Libraries Used

ESP8266WiFi.h 


ESPAsyncWebServer.h 


Adafruit_Sensor.h 


DHT.h 

# Code Description
The setup() function connects the ESP8266 to Wi-Fi using the provided ssid and password. It also initializes the DHT sensor and sets up the web server routes. The web server hosts an HTML page that displays temperature and humidity. The 
loop() function updates the sensor readings every 10 seconds. It reads the temperature and humidity, checks for reading failures, and updates global variables t and h. The web page uses JavaScript to make AJAX calls to 
/temperature and /humidity endpoints to fetch the updated values without refreshing the page.
