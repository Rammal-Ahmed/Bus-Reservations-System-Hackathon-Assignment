# Smart Bus Ticket Booking & Reservation System

A clean, menu-driven command-line application that lets passengers explore bus routes, reserve seats, cancel bookings, and review reservation reports, all built with core Python.

## Purpose

This project demonstrates how a real-world reservation workflow can be modelled with simple, readable code. It manages routes, seat inventory, passenger bookings, and revenue summaries across five cities: Karachi, Hyderabad, Sukkur, Mirpur Khas, and Lahore.

## Requirements

- Python 3.8 or later
- No external libraries or installations needed

## How to Run

```bash
git clone https://github.com/YOUR-USERNAME/smart-bus-reservation-system.git
cd smart-bus-reservation-system
python main.py
```

## Menu Guide

| Option | Feature | What it does |
|:------:|---------|--------------|
| 1 | View Available Routes | Shows all routes, only routes with free seats, or a schedule grouped by departure city |
| 2 | Search for a Route | Finds routes by route ID or city name (not case-sensitive) |
| 3 | Book a Ticket | Collects passenger details, validates them, confirms the booking, and updates seats |
| 4 | View My Bookings | Lists every booking with its fare and status |
| 5 | Cancel a Booking | Cancels a confirmed booking and restores its seats |
| 6 | View Seat Availability | Displays seat counts with status: Available, Partially Booked, or Fully Booked |
| 7 | Generate Booking Report | Summarises bookings, reserved seats, and confirmed revenue by route |
| 8 | Exit | Closes the application |

## Sample Workflow

1. Choose **1** to browse the available routes.
2. Choose **3** and enter the passenger name, age, route ID (for example `R101`), and number of seats.
3. Note the generated booking ID (for example `B1001`) and the total fare.
4. Choose **4** to confirm the booking appears in the history.
5. Choose **5** and enter the booking ID to cancel it. The seats return to the route.
6. Choose **7** to view the report with updated totals.
7. Choose **8** to exit.

## Key Features

- Input validation for names, ages, route IDs, and seat counts
- Unique booking IDs that are never reused, even after cancellation
- Automatic seat deduction on booking and restoration on cancellation
- Protection against overbooking and double cancellation
- Report totals count only confirmed bookings, with cancelled ones tracked separately

## Storage Limitation

This application stores all data **in memory** using Python lists and dictionaries. Bookings and seat changes are **not saved** when the program closes. Every new session starts fresh with the original route data.

## Constraints

- No file or database storage, so records do not persist between runs
- Single-user, single-session operation
- No login or passenger accounts
- Seats are managed as a count; individual seat numbers cannot be chosen
- Routes and fares are fixed in the source code

## Project Structure

```
smart-bus-reservation-system
├── main.py
├── README.md
├── test_cases.txt
└── screenshots/
```

## Possible Future Improvements

- Save bookings to a JSON, CSV, or SQLite file
- Individual seat selection
- Passenger login and booking lookup by phone number
- A graphical or web interface

## Author

Rammal Ahmed
LinkedIn: www.linkedin.com/in/rammal-ahmed-58184b325
GitHub: https://github.com/Rammal-Ahmed
