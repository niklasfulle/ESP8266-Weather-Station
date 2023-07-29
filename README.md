# ESP8266-Weather-Station

## Table of contents

- [Overview](#overview)
- [ESP8266](#esp8266)
  - [Function](#function)
  - [Build](#build)
  - [Dependencies](#dependencies)
- [Backend](#backend)
  - [Function](#function)
  - [Build](#build)
  - [Dependencies](#dependencies)
- [Frontend](#frontend)
  - [Function](#function)
  - [Build](#build)
  - [Dependencies](#dependencies)
- [Images](#images)

## Overview

This project is a weather station that uses an ESP8266 to collect data from a BME280 sensor and send it to a backend server. The backend server then stores the data in a database and serves it to a frontend web application. The frontend web application displays the data in a graph and allows the user to change the units of measurement.

## ESP8266

### Function

The ESP8266 collects data from a BME280 sensor and sends it to a backend server. The ESP8266 is programmed using the Arduino IDE. It works by connecting to a WiFi network and sending a HTTP POST request to the backend server every 15 minutes. The HTTP POST request contains the temperature, humidity, and pressure data from the BME280 sensor. The ESP8266 is powered by three AA batteries. The ESP8266 is put into deep sleep mode after sending the HTTP POST request to save power. The ESP8266 is woken up by a timer interrupt every 15 minutes.

### Build

### Dependencies

| Name | Version | Link |
| ---- | ------- | ---- |
|      |         |      |

## Backend

### Function

The backend server receives data from the ESP8266 and stores it in a database. The backend server is written in Node.js and uses the Express.js framework. The backend server is written in TypeScript and compiled to JavaScript. The backend server uses MongoDb as the database with mongoose and typegoose.

### Build

1. Clone the repository

```bash
git clone https://github.com/niklasfulle/ESP8266-Weather-Station.git
```

2. Navigate to the backend directory

```bash
cd backend
```

3. Install dependencies

```bash
npm i
```

4. Create a .env file in the root directory and add the following environment variables

```bash
PORT=3000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=password
DB_NAME=weather_station
```

5. Start the server

```bash
npm run dev
```

### Dependencies

| Name       | Version | Link                                    |
| ---------- | ------- | --------------------------------------- |
| Node.js    | 18.16.0 | [Link](https://nodejs.org/en/)          |
| TypeScript | 5.1.6   | [Link](https://www.typescriptlang.org/) |

## Frontend

### Function

The frontend web application displays the data from the backend server in a graph.

### Build

1. Navigate to the frontend directory

```bash
cd frontend
```

2. Install dependencies

```bash
npm i
```

3. Create a .env file in the root directory and add the following environment variables

```bash
REACT_APP_API_URL=http://localhost:3000
```

4. Start the server

```bash
npm run dev
```

### Dependencies

| Name       | Version | Link                                    |
| ---------- | ------- | --------------------------------------- |
| Node.js    | 18.16.0 | [Link](https://nodejs.org/en/)          |
| TypeScript | 5.1.6   | [Link](https://www.typescriptlang.org/) |
| React      | 18.2.0  | [Link](https://reactjs.org/)            |
| react-dom  | 18.2.0  | [Link](https://reactjs.org/)            |
| Next.js    | 13.4    | [Link](https://nextjs.org/)             |
| Chart.js   | 3.7.0   | [Link](https://www.chartjs.org/)        |

### Images
