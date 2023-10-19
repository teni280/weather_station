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


## How it works

Using a DHT11, the temeparture and humidity of the surrounding environment is read and the data is pasrsed to host on a local host server.

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

2. Upload the arduino code in sketch_oct9.ino to your ESP32 using Arduino IDE. Once uploaded close VS code

3. In vs code with this respoitroy in the terminal run the code in the terminal type in:
   ```bash
   node script.js

## References

HTML: Learn more about HTML, the standard markup language for creating web pages.
CSS: Explore Cascading Style Sheets (CSS) for styling web pages.
JavaScript: JavaScript is a versatile programming language used for web development.
Socket.IO: Socket.IO is a JavaScript library for real-time web applications. You can find documentation and guides on their website.
