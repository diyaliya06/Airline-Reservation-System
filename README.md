# velvetbluechip Air Reservation System

This README provides an overview of the velvetbluechip air reservation system, outlining its features and functionality.

## Overview

The velvetbluechip air reservation system is a web-based platform designed to allow users to book flights, manage their trips, explore offers, check-in for flights, and learn about the VelvetBlueChip loyalty program. The system features a user-friendly interface with a login system to access the main functionalities.

## Features

* **User Authentication:** Secure login for users to access personalized features.
* **Flight Booking:**
    * Supports one-way, round-trip, and multi-city flight searches.
    * Allows users to specify origin, destination, departure and return dates, number of passengers, and travel class.
    * Includes a section for selecting the reason for travel and preferred payment method.
    * Integration point for applying promocodes.
    * "Search Flights" functionality (currently simulated with an alert and redirection).
* **Trip Management:** A dedicated section for users to view and manage their upcoming and past trips. Includes a link to a "Manage Reservations" page.
* **Offers and Discounts:** A section showcasing the latest flight offers and discounts, with a link to a dedicated "offers" page.
* **Online Check-in:** A page for users to perform online check-in for their flights.
* **VelvetBlueChip Loyalty Program:** Information about the airline's loyalty program, with a link to a dedicated "VelvetBlueChip" page.
* **Lower Fare Exploration:** Displays a section with cards showcasing popular routes with potentially lower fares, including images and "Book Now" buttons that redirect to a booking page.
* **Retrieve Booking via PNR:** A separate section allowing users to retrieve their booking details using their PNR (Passenger Name Record) or booking reference and either their email ID or last name.

## Technologies Used

* **HTML:** For structuring the web page content.
* **CSS:** For styling the user interface, including responsive design using Bootstrap.
* **JavaScript:** For implementing interactive elements and handling user actions, leveraging jQuery for DOM manipulation.
* **Bootstrap:** A CSS framework to provide pre-built styles and components for a responsive layout.
* **Font Awesome:** An icon toolkit used for visual elements.
* **jQuery:** A JavaScript library to simplify DOM traversal, event handling, and AJAX interactions.

## Structure

The HTML file is structured into the following main sections:

1.  **Login View (`#loginView`):** A form for user login with username and password fields.
2.  **Main View (`#mainView`):** The primary interface after successful login, containing:
    * A welcome message.
    * A tab navigation (`.tabs-nav`) to access different sections (Book, Trips, Offers, Check-in, VelvetBlueChip).
    * Tab content areas (`.tabs-content`) for each section.
    * A flight booking widget with options for one-way, round-trip, and multi-city bookings.
    * Input fields for flight details (origin, destination, dates, passengers, class).
    * Dropdowns for travel reason and payment method.
    * Buttons for adding a promocode and searching for flights.
    * A section displaying lower fare routes with "Book Now" buttons.
3.  **Find Booking View (`#findBookingView`):** A form allowing users to retrieve their booking using their PNR and email or last name.

## JavaScript Functionality

The JavaScript code handles the following:

* **Login:** Submitting the login form, validating credentials (client-side simulation), and transitioning to the main view upon successful "login."
* **Tab Navigation:** Switching between the different sections of the main view when a tab button is clicked.
* **Flight Booking Options:** Handling the selection of booking types (one-way, round-trip, multi-city) and updating the form accordingly (e.g., enabling/disabling the return date field).
* **Lower Fare "Book Now":** Redirecting to a `booking.html` page when a "Book Now" button in the lower fares section is clicked.
* **Flight Search:** Handling the "Search Flights" button click, displaying an alert with the entered flight details, and redirecting to a `confirmation.html` page (simulated functionality). It also includes a specific redirect to a `paypal_payment.html` page if "PayPal" is selected as the payment method.

## Notes

* The provided code includes client-side scripting for basic interactions and form handling. It does not contain actual backend logic for user authentication, flight data retrieval, or booking processing.
* The redirects to `booking.html`, `offers.html`, `confirmation.html`, `paypal_payment.html`, `manage_reservations.html`, and `VelvetBlueChip.html` are placeholders and would need to be implemented with actual pages in a complete system.
* The multi-city booking option currently logs a message to the console; the implementation of dynamic fields for multi-city searches would require further development.
* The login validation is a basic client-side check and should be implemented with proper server-side authentication in a production environment.
