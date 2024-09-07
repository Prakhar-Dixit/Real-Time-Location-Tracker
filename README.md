# Real-Time Location Tracker

![Real-Time Location Tracker](![Screenshot 2024-09-07 131420](https://github.com/user-attachments/assets/f62c6073-66ce-41a1-a922-1aa02265d0b5))

A simple real-time location tracking application built using Node.js, Express, Socket.IO, and Leaflet.js. This project demonstrates the use of WebSockets for real-time communication, allowing users to share their location data and visualize it on a live map.

## Features

- **Real-Time Location Sharing**: Users can share their current location, which is updated on the map in real-time.
- **Live Map Visualization**: The app uses Leaflet.js to display an interactive map with markers showing the locations of connected users.
- **Dynamic User Management**: The map dynamically updates as users connect and disconnect, adding or removing markers accordingly.

## Technologies Used

- **Node.js**: JavaScript runtime used to build the server-side application.
- **Express**: A minimal and flexible Node.js web application framework.
- **Socket.IO**: A library that enables real-time, bidirectional, and event-based communication.
- **Leaflet.js**: An open-source JavaScript library for mobile-friendly interactive maps.
- **EJS**: Embedded JavaScript templates for rendering HTML.

## Project Structure

- **app.js**: The main server file, responsible for setting up the Express app, configuring Socket.IO, and handling events.
- **views/index.ejs**: The front-end view rendered by Express, which includes the map and client-side JavaScript.
- **public/js/script.js**: The client-side JavaScript file that handles location tracking, socket communication, and map interactions.
- **public/css/style.css**: The CSS file for basic styling of the application.

## Setup and Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/real-time-location-tracker.git
    ```
2. Navigate to the project directory:
    ```bash
    cd real-time-location-tracker
    ```
3. Install the dependencies:
    ```bash
    npm install
    ```
4. Start the server:
    ```bash
    npm start
    ```
5. Open your browser and go to `http://localhost:3000` to view the application.

## How It Works

1. **User Connection**: When a user connects to the application, they are assigned a unique socket ID. Their location data is then tracked and emitted to the server.
2. **Location Broadcast**: The server listens for `send-location` events from connected clients and broadcasts the received location data to all connected clients.
3. **Map Update**: Each client receives the location data and updates the map, either adding a new marker or updating an existing one.
4. **User Disconnection**: When a user disconnects, the server notifies all clients to remove the marker associated with that user from the map.

## Contributing

Feel free to submit issues or pull requests if you find any bugs or have suggestions for improvements.
