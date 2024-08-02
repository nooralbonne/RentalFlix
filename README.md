# RentalFlix ERD

## Overview

This repository contains the Entity-Relationship Diagram (ERD) for the "RentalFlix" movie rental service. The purpose of this diagram is to model the key entities and relationships needed to manage movie rentals, customer information, and reservations efficiently.

## Project Specifications

**RentalFlix** is designed to replace an outdated movie rental system with a modern, digital solution. The system manages:
- Movies and their formats
- Customer information
- Rental records
- Movie reservations

## Entities and Relationships

### Entities

1. **Movie**
   - **MovieID** (PK): Unique identifier for each movie.
   - **Title**: Title of the movie.
   - **Genre**: Genre or category of the movie.
   - **Director**: Director of the movie.
   - **ReleaseYear**: Year the movie was released.
   - **Rating**: Movie rating (e.g., PG, PG-13, R).

2. **MovieFormat**
   - **FormatID** (PK): Unique identifier for each movie format.
   - **MovieID** (FK): Identifier of the movie.
   - **FormatType**: Type of format (DVD, Blu-ray, Digital).
   - **QuantityAvailable**: Number of copies available for rent.

3. **Customer**
   - **CustomerID** (PK): Unique identifier for each customer.
   - **Name**: Name of the customer.
   - **Address**: Address of the customer.
   - **Phone**: Contact phone number.
   - **Email**: Contact email address.

4. **Rental**
   - **RentalID** (PK): Unique identifier for each rental record.
   - **CustomerID** (FK): ID of the customer who rented the movie.
   - **FormatID** (FK): ID of the movie format that was rented.
   - **RentalDate**: Date when the movie was rented.
   - **DueDate**: The date when the movie is due to be returned.
   - **ReturnDate**: Date when the movie was returned (nullable).

5. **Reservation**
   - **ReservationID** (PK): Unique identifier for each reservation.
   - **CustomerID** (FK): ID of the customer who reserved the movie.
   - **MovieID** (FK): ID of the reserved movie.
   - **ReservationDate**: Date when the reservation was made.
   - **Status**: Status of the reservation (active, fulfilled, canceled).

### Relationships

- **Movie** to **MovieFormat**: One-to-Many
- **Customer** to **Rental**: One-to-Many
- **Rental** to **MovieFormat**: Many-to-One
- **Movie** to **Reservation**: One-to-Many
- **Reservation** to **Customer**: Many-to-One

## ERD Diagram

Below is the Entity-Relationship Diagram for the RentalFlix system:

![ERD Diagram](https://github.com/nooralbonne/RentalFlix/blob/master/ERDdiagram-.png)

## Submission Instructions

1. Create a new repository named `RentalFlix` on GitHub.
2. Create a branch named `RentalFlixERD`.
3. Add the ERD diagram image and this README.md file to the repository.
4. Commit your changes and push them to the `RentalFlixERD` branch.
5. Create a pull request from the `RentalFlixERD` branch to the main branch.
6. Submit the link to your pull request in the submission field.

## Contact

For any questions or feedback, please contact [Noor Albonne](nooralbonne@gmail.com).

