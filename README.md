Hotel Reservation System
A basic console-based hotel reservation system built in Java using JDBC and MySQL.
This project allows hotel staff to manage room bookings, view existing reservations, update details, and delete bookings.

Tech Stack
Java (JDK 17+ or higher)
JDBC for database connectivity
MySQL (local server)
IntelliJ IDEA or Eclipse
Features
Reserve a room (guest name, room number, contact)
View all current reservations in a table format
Update an existing reservation
Delete a reservation
MySQL database integration
Database Schema

CREATE DATABASE hotel_db;

USE hotel_db;

CREATE TABLE reservations (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY,
    guest_name VARCHAR(100),
    room_number INT,
    contact_number VARCHAR(15),
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
How to Run
Make sure MySQL is running on port 3306 or update it in the code.

Update your database credentials in HotelReservationSystem.java:

private static final String url = "jdbc:mysql://localhost:3306/hotel_db";
private static final String user = "root";
private static final String password = "your_password";
Compile and run the project from IntelliJ or using:

javac -cp .:mysql-connector-j-<version>.jar HotelReservationSystem.java
java -cp .:mysql-connector-j-<version>.jar HotelReservationSystem
