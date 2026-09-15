# Room Rental System

This is a simple Java console application designed to manage room reservations for students in a boarding house. It allows the user to register a specific number of students, assign them to chosen rooms, and then generates a report showing all currently occupied rooms.

## Project Structure

The project is divided into two primary files:

* **`Program.java`**: The main entry point of the application. It handles user inputs (validating the number of students to register), collects the student's details (name, email) along with their desired room number, and prints the final report of busy rooms to the console.
* **`Rent.java`**: An entity class representing the rental record. It encapsulates the student's data fields (`name`, `email`) and provides an overridden `toString()` method to easily format the output.

## Features and Logic

The application relies on core programming concepts to manage the data:

1. **Array-Based Storage**: The system uses a fixed-size array of 10 elements to represent the available rooms. The room number chosen by the user acts directly as the index in the array (`vect[roomNumber]`).
2. **Input Validation**: The program uses a `while(true)` loop to ensure the user inputs a valid number of students (between 1 and 10) before proceeding, preventing out-of-bounds errors.
3. **Null-Checking Logic**: To display the final report, the system iterates through the array and checks for `null` elements. If an array position is not null, it means the room is occupied and its data is printed.

## Execution Example

```text
How many rooms will be rented? 2
Rent #1:
Name: Maria Green
Email: maria@gmail.com
Room: 5
Rent #2:
Name: Marco Antonio
Email: marco@gmail.com
Room: 1

Busy rooms:
1: Marco Antonio, marco@gmail.com
5: Maria Green, maria@gmail.com
```
