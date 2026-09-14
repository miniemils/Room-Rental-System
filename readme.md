# Room Rental System

This is a Java console application designed to manage room assignments for a student boarding house. The program utilizes arrays to allocate specific rooms to students based on user input, ensuring data is mapped to the correct room number.

## Project Overview

The application prompts the user for the number of students who will be renting rooms (between 1 and 10). For each student, the system collects their name, email, and desired room number. It then assigns the student's data to the chosen room and finally prints a report showing all occupied rooms.

## Project Structure

The project is organized into two main files:

* **`Program.java`**: The main execution script. It handles the user interface via the console, validates the initial input (ensuring the number of students is between 1 and 10), and manages the array of rooms.
* **`Rent.java`**: The entity class representing a rental agreement. It encapsulates the student's `name` and `email`, providing getters and a custom `toString()` method for formatting the output.

## How it Works

The core logic relies on an array of objects:
1. **Array Instantiation:** The system creates an array `Rent[] vect = new Rent[10]`, representing up to 10 available rooms.
2. **Data Allocation:** When a user selects a room number, the program instantiates a new `Rent` object and places it directly into the array at the index corresponding to the chosen room number (`vect[roomNumber] = r;`).
3. **Null Checking:** To print the final report, the program iterates through the array. It checks if an index is not null (`if(vect[i] != null)`) to determine if a room is occupied before printing its details.

## How to Run

1. Make sure you have Java installed on your computer.
2. Open your terminal and navigate to the project's root folder.
3. Compile the Java files (assuming they are in `application` and `entities` packages):
   ```bash
   javac application/Program.java entities/Rent.java
   ```
4. Run the program:
   ```bash
   java application.Program
   ```
5. Follow the console prompts. Remember that the program uses the US locale.