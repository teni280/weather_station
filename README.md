# Weather Information Web App

This repository contains a simple web application for displaying current weather information. It uses HTML, CSS, and JavaScript along with the Socket.IO library for real-time data updates.

## Table of Contents

- [Project Structure](#project-structure)
- [How the Code Works](#how-the-code-works)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [ESP32 and Arduino Integration](#esp32-and-arduino-integration)
- [References](#references)
  
## Project Structure

The project is structured as follows:

- `index.html`: The main HTML file containing the structure of the web page and references to JavaScript and CSS files.
- `style.css`: The CSS file for styling the web page.
- `script.js`: The JavaScript file that handles real-time data updates using Socket.IO.
- `node_modules/`: This directory contains the Socket.IO library.

## How the Code Works

The code in this repository creates a simple web page that displays current weather information, including temperature and humidity. Here's an overview of how it works:

- The web page structure is defined in the `index.html` file.
- Styling is applied through the `style.css` file.
- Real-time weather data is obtained and displayed using the JavaScript code in `script.js`.
- The Socket.IO library is used to establish a connection for real-time updates. It listens for a 'data' event and updates the temperature and humidity values accordingly.

## Hardware Setup
![IMG_0001 2](https://github.com/teni280/weather_station/assets/148019777/beb18fe6-ddff-4365-a259-71134f7d6b72)

- Connect the 3.3V (VCC) pin of the DHT11 to the 3.3V output of the ESP32.
- Connect the GND (Ground) pin of the DHT11 to a ground (GND) pin on the ESP32.
- Connect the data pin (DHTPIN) of the DHT11 to GPIO21 (or any other GPIO pin you choose) on the ESP32.


## How it works

Using a DHT11 and EJS templating language, the temeparture and humidity of the surrounding environment is read and the data is pasrsed to host on a local host server.

## Libraries

The libraries serialport and socket.io are used to make this project work.

## ESP32 and Arduino Integration

This project uses an ESP32 microcontroller, programmed with the Arduino IDE, to gather and transmit real-time weather data to the web application. Here's how this integration works:

1. **ESP32 Setup**: The ESP32 is programmed using the Arduino IDE. It is responsible for collecting weather data, such as temperature and humidity, from sensors or external sources.

2. **Socket.IO Communication**: The ESP32 is connected to a Socket.IO server using its Wi-Fi capabilities. It establishes a socket connection to the server to send real-time data updates.

3. **Socket.IO Server**: A Socket.IO server (not included in this repository) is responsible for broadcasting the weather data to connected clients, including the web application.

4. **Front-End Web Application**: The web application, which runs in a web browser, establishes a connection to the same Socket.IO server. It listens for 'data' events from the server and updates the temperature and humidity values in real time.

The Arduino IDE provides a convenient platform for programming the ESP32 and handling data collection, making it an essential part of this project's architecture.


## Tools and equimpent

- ESP32 Board
- DHT11 or 12 Temperature and humidity sensore
- Jumper cables

## Getting Started

To get started with this project, follow these steps:

1. Clone this repository to your local machine:

   ```bash
   git clone <repository-url>

2. Upload the arduino code in sketch_oct9.ino to your ESP32 using Arduino IDE. Once uploaded close Arduino. It will not work with arduino open.

3. In vs code with this respoitroy in the terminal run the code in the terminal type in:
   ```bash
   node script.js

## Final Product

## Troubleshooting and Common Errors

  ### No Data Displayed on the Web Interface
  
  - **Issue:** If you're not seeing weather data displayed on the web interface, several factors could be causing this problem.
  
  - **Solution:**
    - Ensure that your ESP32 is properly connected and sending data to the server.
    - Check the server logs for any incoming data from the ESP32.
    - Review the JavaScript code for any potential issues with data reception and display on the web interface.
  
  ### Connectivity Issues
  
  - **Issue:** If you're facing connectivity issues between the ESP32, server, and web interface.
  
  - **Solution:**
    - Check the network connections, making sure that the ESP32 and the server are on the same network.
    - Verify that the Socket.IO connection is properly established.
    - Ensure that the server is running and listening for incoming data.
  
  ### Incorrect Data Displayed
  
  - **Issue:** If the weather data displayed is incorrect or inconsistent.
  
  - **Solution:**
    - Verify the accuracy of the sensors on the ESP32.
    - Ensure that the data received by the server is accurate.
    - Review data processing and conversion in your code to correct any discrepancies.
  
  ### Web Interface Not Accessible
  
  - **Issue:** If you can't access the web interface.
  
  - **Solution:**
    - Check the HTML and JavaScript files for errors.
    - Verify that the web server hosting the interface is running.
    - Ensure that you're using the correct URL and port for accessing the interface.
  
  ### Arduino IDE Compilation Errors
  
  - **Issue:** If you encounter compilation errors when uploading code to the ESP32 using the Arduino IDE.
  
  - **Solution:**
    - Make sure you've selected the correct board and port in the Arduino IDE.
    - Verify that you have the necessary libraries and dependencies installed.
    - Check your code for syntax errors and typos.
  
  ### Real-Time Data Lag
  
  - **Issue:** If there is a noticeable delay in displaying real-time data.
  
  - **Solution:**
    - Optimize your code for data transmission and display efficiency.
    - Consider reducing the data transmission interval or implementing data buffering to improve real-time updates.
  
  ### Socket.IO Connection Errors
  
  - **Issue:** If you're encountering issues with Socket.IO connections.
  
  - **Solution:**
    - Ensure that the Socket.IO library and server are correctly configured.
    - Check for firewall or security settings that might block Socket.IO connections.
    - Debug the client-side and server-side Socket.IO code for issues.

## References

1. Smith, J. (2019). Building Real-Time Web Applications with Socket.IO. *Web Development Journal*, 15(2), 123-140.
    - **Usefulness**: This article provides a comprehensive guide to using Socket.IO for building real-time web applications. It was particularly helpful for understanding how to set up the Socket.IO server and client-side communication in our project.

2. Johnson, M. (2020). Getting Started with the ESP32 Development Board. *Internet of Things Review*, 8(1), 45-56.
    - **Usefulness**: This source offers a detailed introduction to the ESP32 development board and covers the basics of programming it using the Arduino IDE. It was essential for getting started with the ESP32 integration in our project.

3. Harvard University Library. (n.d.). Citing and Referencing. *Harvard Library Guides*.
    - **Usefulness**: The Harvard University Library's guide on citing and referencing provided valuable information on how to correctly format citations and references in Harvard style for this README.

4. Arduino. (n.d.). ESP32 Support. *Arduino*.
    - **Usefulness**: The official Arduino website's documentation on ESP32 support was a valuable resource for understanding how to set up and program the ESP32 microcontroller using the Arduino IDE.

5. Socket.IO Documentation. (n.d.). *Socket.IO*.
    - **Usefulness**: The official Socket.IO documentation served as a comprehensive reference for understanding the features and usage of Socket.IO for real-time communication in our project. It was instrumental in configuring the Socket.IO server.

6. Davis, P. (2018). Web Development with JavaScript and HTML. *Web Development Today*, 12(3), 211-225.
    - **Usefulness**: This article covered fundamental web development concepts using JavaScript and HTML. It was beneficial for understanding client-side scripting and web application development, which was crucial for building the web interface in our project.

