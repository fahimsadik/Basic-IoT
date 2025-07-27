# ESP8266 IR Web Remote
This project turns an ESP8266 into a Wi-Fi-enabled universal remote control. It hosts a simple web page with buttons that, when clicked, send specific IR commands to control various devices like a TV or a sound system. This allows you to control your appliances from any device on the same network.

# Components Needed
ESP8266 board (e.g., NodeMCU)

IR LED (to send signals)

IR Receiver (optional, for learning new codes)

Jumper wires

# Circuit Connections
IR LED Anode -> 3.3V

IR LED Cathode -> ESP8266 Digital Pin 

D8 through a current-limiting resistor 

Libraries Used

ESP8266WiFi.h 


IRremoteESP8266.h 


ESP8266WebServer.h 


ESP8266mDNS.h 

# Code Description
The setup() function connects the ESP8266 to Wi-Fi and initializes the web server. It defines routes for each button on the web page, such as /on, /OFF, /tvpower, etc.. 

The handleRoot() function generates the HTML for the web page, which contains the buttons. When a button is clicked, an AJAX call is made to the corresponding server route. The server then uses the 


irsend.sendNEC() function to transmit the pre-defined IR code for that action.
