🚗 DriveEase — Vehicle Rental Platform

A modern, browser-based vehicle rental platform for cars, SUVs, bikes, and scooters. DriveEase provides self-drive rental options, optional professional drivers, customer booking management, and a fleet administration dashboard.

📌 Table of Contents

Overview

Features

Technology Stack

Project Architecture

Project Structure

Pages and User Flows

Data Layer and State Management


🌟 Overview

DriveEase is a front-end vehicle rental application developed using HTML, CSS, and JavaScript.

It provides an end-to-end rental experience, allowing users to browse vehicles, select rental durations, calculate rental costs, and manage bookings.

The application uses JavaScript classes, LocalStorage, custom events, and browser storage synchronization to manage application data.

Note: This is a front-end demonstration project. Data is stored locally in the browser and is not connected to a production backend or shared database.

✨ Features

🚘 1. Vehicle Browsing

Browse cars, SUVs, bikes, and scooters.

Filter vehicles by category and availability.

Search vehicles by name, category, transmission, and fuel type.

View real-time vehicle status indicators:

Available

Booked

Maintenance

🚗 2. Flexible Rental Options

Self-drive rental options for eligible vehicles.

Professional driver service for cars and SUVs.

Driver selection automatically disabled for two-wheelers.

Flexible rental duration from 1 to 30 days.

💰 3. Dynamic Price Calculation

Automatic price calculation based on rental duration.

Additional driver charges of ₹800 per day.

Instant price updates when rental options change.

Transparent price breakdown in Indian Rupees (₹).

👤 4. Customer Dashboard

View total bookings and active rentals.

Track lifetime spending.

View booking history and details.

Cancel eligible pending and active bookings.

Monitor booking status updates.

🛠️ 5. Fleet Admin Dashboard

The administration panel provides the following management modules:

Module

Functionality

Fleet Management

Update vehicle availability and maintenance status.

Booking Management

Manage booking statuses and delete records.

Customer Management

View customer booking counts and lifetime value.

Revenue Analytics

View revenue, average booking value, and vehicle performance.

Driver Management

Add, remove, search, and update driver availability.

Message Management

View customer inquiries and mark messages as read.

🔐 6. Authentication and Validation

Customer registration and login.

Separate customer and administrator login flows.

Real-time input validation and sanitization.

Indian mobile number validation (10 digits starting with 6–9).

Date validation to prevent selecting past dates.

Password confirmation validation.

💻 Technology Stack

Technology

Purpose

HTML5

Structure and content of web pages

CSS3

Styling, layouts, responsiveness, and animations

JavaScript (ES6+)

Application logic and interactivity

LocalStorage

Browser-based data persistence

Object-Oriented Programming

Data models and reusable application logic

DOM Manipulation

Dynamic content rendering and updates

🏗️ Project Architecture

The application follows a modular JavaScript architecture.

                   HTML Pages
                       |
          +------------+------------+
          |                         |
     validate.js                  data.js
  Form Validation            Shared Data Layer
                                    |
          +------------+------------+------------+
          |            |            |            |
      VehicleStore  DriverStore  BookingStore  UserStore
          |            |            |            |
          +------------+------------+------------+
                                    |
                               localStorage
                                    |
               +--------------------+-------------------+
               |                    |                   |
           vehicles.js          booking.js         fleet-admin.js
          Search & Filter     Booking & Pricing    Admin Dashboard

Main JavaScript Modules

data.js: Manages application data, classes, LocalStorage, and authentication.

validate.js: Handles form validation and input sanitization.

vehicles.js: Manages vehicle listings, search, and filtering.

booking.js: Handles booking operations and dynamic price calculations.

fleet-admin.js: Manages administrative operations and analytics.

📁 Project Structure

File

Description

index.html

Homepage with hero section, statistics, and featured vehicles.

vehicles.html

Vehicle catalog with search and category filtering.

vehicles.js

Vehicle rendering, search, filtering, and status synchronization.

booking.html

Booking form with vehicle selection and price summary.

booking.js

Booking functionality and dynamic price calculation.

customer.html

Customer dashboard with booking history and statistics.

fleet-admin.html

Administrative dashboard with multiple management modules.

fleet-admin.js

Admin operations, fleet management, and revenue analytics.

login.html

Customer and administrator login page.

register.html

Customer registration page.

admin_login.html

Shortcut to the administrator login flow.

contact.html

Contact page with customer inquiry form.

data.js

Shared data layer, classes, storage, and authentication helpers.

validate.js

Form validation and input sanitization utilities.

style.css

Global stylesheet and responsive layouts.

vehicle-activa.html

Honda Activa 6G vehicle details.

vehicle-classic350.html

Royal Enfield Classic 350 vehicle details.

vehicle-creta.html

Hyundai Creta vehicle details.

vehicle-nexon.html

Tata Nexon vehicle details.

vehicle-swift.html

Maruti Swift vehicle details.

🖥️ Pages and User Flows

1. Public Vehicle Browsing

Open index.html to access the homepage.

Navigate to vehicles.html to explore the fleet.

Search vehicles by name, fuel type, or transmission.

Filter vehicles using category tabs.

Check vehicle availability before booking.

2. Vehicle Details

Dedicated vehicle pages provide information about specifications, features, and rental options.

Available vehicle pages:

vehicle-activa.html

vehicle-classic350.html

vehicle-creta.html

vehicle-nexon.html

vehicle-swift.html

Vehicle availability is synchronized with the shared data layer.

3. Booking Workflow

Open booking.html.

Select a vehicle.

Choose the rental duration.

Select the professional driver option if eligible.

Review the automatically calculated rental cost.

Submit the booking.

Example booking URLs:

booking.html?vehicle=creta

booking.html?vehicle=creta&driver=1&driverId=d1

Customer details are automatically populated when a customer is logged in.

4. Customer Dashboard

Open customer.html after logging in.

View booking history and current booking statuses.

Click a booking to view its details.

Cancel eligible bookings.

5. Fleet Admin Dashboard

Open fleet-admin.html or access the administrator login flow through login.html?role=admin.

Administrators can:

Update vehicle statuses.

Manage customer bookings.

View customer information.

Monitor revenue analytics.

Manage drivers and their availability.

Review customer inquiries.

6. Authentication and Registration

Use login.html for customer or administrator login.

Use register.html to create a new customer account.

Registration includes password confirmation and input validation.

7. Contact and Support

Use contact.html to submit inquiries. Messages are stored locally and can be reviewed through the admin dashboard.
