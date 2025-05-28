# Ticket Nexus: A Command-Line Ticket Booking System

Ticket Nexus is a modular, object-oriented C++ application designed to streamline transportation and entertainment ticketing via a robust command-line interface. It automates and secures the entire booking lifecycle—from login and user role validation to real-time seat management and ticket issuance—addressing the inefficiencies of manual systems while laying the foundation for future extensions into broader domains such as airlines and live events.

---

## Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Features and Scope](#features-and-scope)
- [Limitations](#limitations)
- [Significance](#significance)
- [Technologies Used](#technologies-used)
- [Development Strategy](#development-strategy)
- [Installation and Setup](#installation-and-setup)
- [Usage](#usage)
- [Directory Structure](#directory-structure)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Overview

Ticket Nexus is a command-line ticket booking system crafted exclusively in C++, optimized for terminal-based environments. The design emphasizes modularity and object-oriented principles to deliver a maintainable software solution that efficiently handles ticket reservations for buses and movies. Its architecture ensures that every aspect—from user authentication to dynamic seat mapping—is clearly organized into discrete, reusable modules, ensuring seamless extensibility and ease of maintenance.

---

## Problem Statement

Manual ticket reservation processes for bus and movie services are often plagued with issues such as booking conflicts, data redundancy, and limited accessibility. The absence of a centralized system complicates:
- **Tracking seat availability**
- **Validating user inputs**
- **Handling different user roles securely**

Ticket Nexus addresses these challenges by introducing an automated, file-based solution that manages role-based access, enforces real-time seat tracking, and simplifies ticket management operations—all from a command-line interface.

---

## Objectives

1. **CLI-Based Ticket Booking:** Develop a command-line application that supports two distinct user roles—Admin and User.
2. **Comprehensive Data Management:** Enable Admins to add, edit, delete, and search bus and movie records.
3. **Tracking and Monitoring:** Allow Admins to view booking histories and monitor overall booking activity.
4. **User Flexibility:** Grant Users the ability to search, book, and cancel tickets with ease.
5. **Secure Authentication:** Implement robust, role-based access control using secure credential handling and dynamic validation.
6. **Prevention of Double Bookings:** Integrate dynamic seat maps that provide real-time seat validation during ticket selection.
7. **Data Persistence:** Maintain data consistency and persistence through structured, pipe-delimited text files.
8. **Robust Input Validation:** Ensure data integrity by validating critical fields such as dates, times, and phone numbers.

---

## Features and Scope

- **Role-Based Authentication:** Supports secure login for both Admin and User accounts through flexible identifiers (username, email, or phone number).
- **Dynamic Ticket Booking:** Real-time tracking of bus and movie reservations with automated prevention of overlapping seat bookings.
- **Admin Controls:** 
  - Predefined Admin account (not re-registerable via sign-up).
  - Ability to add, edit, and delete records for bus and movie services.
  - View comprehensive booking logs and history.
- **User Capabilities:**
  - Search for bus/movie services.
  - Book and cancel tickets.
  - View personal booking history.
- **Real-Time Seat Management:** Dynamic seat maps with color-coded availability and input validation to avoid double booking.
- **File-Based Data Persistence:** Uses structured, pipe-delimited text files for storing user, booking, and service records.
- **Booking Validation:** Ensures that bookings are limited to current or future dates, automatically rejecting any past-dated reservations.

---

## Limitations

- **Command-Line Interface Only:** All interactions are conducted via the terminal; there is no graphical user interface.
- **File-Based Storage:** Data is managed through plain text files rather than a relational database system.
- **Simulated Payment Processing:** Payment functionalities are simulated and do not involve actual transaction integrations.

---

## Significance

Ticket Nexus transforms a traditionally cumbersome manual booking process into an organized, automated system—enhancing:
- **Operational Efficiency:** Automates complex ticketing operations with clear role segregation.
- **Data Integrity:** Utilizes rigorous input validation and secure storage practices (e.g., hashed credentials).
- **User Experience:** Prevents overbooking and ensures accurate seat availability through dynamic maps.
- **Accountability:** Each booking is uniquely timestamped and traceable for thorough record-keeping.

---

## Technologies Used

- **Language:** C++
- **Paradigm:** Object-Oriented Programming
- **Interface:** Command-Line/Terminal
- **Data Handling:** File-based persistence using structured, pipe-delimited text files
- **Compilation:** Standard C++ compiler (e.g., g++)

---

## Development Strategy

### Programming Environment

**Development Environment:**
- **Programming Language:** C++ (Standard: C++13)
- **IDE/Editors Used:** Visual Studio 2019, Dev-C++
- **Compiler:** MSVC (Visual Studio), MinGW (g++)
- **Operating System:** Windows 10 / Windows 11

**Libraries/Dependencies:**
- `<iostream>` – Standard input/output operations
- `<string>` – String manipulations
- `<fstream>` – File I/O for persistent storage
- `<windows.h>` – Windows API functions for color and console manipulation
- `<ctime>` – Timestamp generation for bookings
- `<sstream>` – String stream conversions
- `<conio.h>` – Console input handling (e.g., _getch() for password masking)
- `<iomanip>` – Output formatting (e.g., field width, precision)
- `"Color.h"` – Custom header for terminal text coloring
- `"Validation.h"` – Custom header for input validation (e.g., dates, names, formats)
- `"menu.h"` – Custom header for rendering and handling interactive CLI menus
- `"wait.h"` – Custom header for wait functions, cursor control, and loading animations

**Build System:** Manual compilation via IDE or command-line using g++

**Data Storage:** Text files using pipe (`|`) delimiters for structured persistence

**Interface:** Command-Line Interface (CLI) only

---

## Installation and Setup

### Prerequisites

- **C++ Compiler:** Ensure you have a modern C++ compiler installed (e.g., g++ version 7 or later).
- **Build Tools:** Optionally, install GNU Make if you prefer using a Makefile for the build process.
- **Environment:** A terminal or command-line interface on your machine.

### Compilation

1. **Using g++ Directly:**

   ```bash
   g++ -std=c++17 main.cpp -o TicketNexus
