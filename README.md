# Football Ticket Booking Database - L2B7A3

A simple PostgreSQL database project for managing football matches, users, and ticket bookings.

## Overview

This project demonstrates how to design a relational database and write SQL queries for a football ticket booking system.

It includes:

* Users
* Football matches
* Ticket bookings
* Payment status
* Seat information
* Ticket prices

## Database Structure

The database contains three main tables:

```text
┌──────────────┐
│    Users     │
├──────────────┤
│ PK user_id   │
│ full_name    │
│ email        │
│ role         │
│ phone_number │
└──────┬───────┘
       │
       │ 1
       │
       │ N
┌──────▼───────┐
│   Bookings   │
├──────────────┤
│ PK booking_id│
│ FK user_id   │
│ FK match_id  │
│ seat_number  │
│ payment_status│
│ total_cost   │
└──────┬───────┘
       │
       │ N
       │
       │ 1
┌──────▼─────────────┐
│      Matches       │
├────────────────────┤
│ PK match_id        │
│ fixture            │
│ tournament_category│
│ base_ticket_price  │
│ match_status       │
└────────────────────┘
```

### Relationships

* One user can have many bookings.
* One match can have many bookings.
* Each booking belongs to one user.
* Each booking belongs to one match.

## SQL Concepts

The project covers common and useful SQL concepts, including:

* Primary Keys
* Foreign Keys
* Table Relationships
* `JOIN`
* `LEFT JOIN`
* Subqueries
* Aggregate Functions
* `COUNT`
* `AVG`
* `LIKE`
* `ILIKE`
* `COALESCE`
* `NULL` handling
* Sorting
* Pagination

## Project Structure

```text
football-ticket-booking-database/
├── QUERY.sql
├── README.md
└── ERD
```

## Technologies

* PostgreSQL
* SQL
* ERD

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/mrshanshuvo/football-ticket-booking-database.git
```

### 2. Create the database

```sql
CREATE DATABASE football_ticket_booking;
```

### 3. Connect to PostgreSQL

```bash
psql -U postgres -d football_ticket_booking
```

### 4. Run the SQL file

Run the queries from:

```text
QUERY.sql
```

## Learning Goals

This project helped practice:

* Relational database design
* ERD creation
* PostgreSQL
* SQL queries
* Table relationships
* Data retrieval and filtering
* Joins and subqueries

## License

This project is for educational purposes.
