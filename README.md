# Python-Essentials-Project

# Hostel Room Allocation System


## Overview of the Project
The Hostel Room Allocation System is a simple, menu-driven Python application that helps hostel authorities manage rooms and students.  
Instead of writing everything in registers or Excel sheets, this system stores room details and student information in memory and allocates rooms automatically based on gender and available capacity.  
It also records the date on which a student is allotted a room, making it easier to keep proper records.

The project is built using basic Python and object-oriented programming concepts and runs completely in the terminal/command prompt.



## Features

Add Room  
  Add new rooms with room number, capacity, and gender type (M/F).

View Rooms 
  Display all rooms along with their capacity, gender type, and current number of occupants.

Add Student 
  Add student details such as ID, name, gender, year, and course.

View Studen  
  Display all students with their allocated room number and allocation date.
Allocate Room
  Automatically assign a room to a student based on:
  - matching gender (M/F)
  - available capacity in the room  
  Also stores the date of allocation using the current system date.

Deallocate Room 
  Remove a student from a room and clear their room and allocation date.

Clear All Data 
  Delete all room and student records from the system.
Exit
  Close the application safely.

---

## Technologies 

Programming Language: Python 3  
Editor: Visual Studio Code 
Python Standard Libraries:
 `datetime` – to store the allocation date  
 `typing` – for type hints (`List`, `Dict`, `Optional`)

---

## Steps to Install & Run the Project

1. Install Python 3
   - Make sure Python 3 is installed on your system.
   - You can check using:
     ```bash
     python --version
     ```
     or
     ```bash
     python3 --version
     ```

2. Download 
   - Download the project folder or clone it from GitHub into your system.

3. Open the Project Folder
   - Open the folder in VS Code or navigate to it in terminal

4. Run the Python File
   - Make sure your main file (with the code) is saved as something like:
     
     Hostel_System.py
     
   - In terminal, run:
     ```bash
     python Hostel_System.py
     ```

5. Use the Menu
   - A text menu called HOSTEL MENU will appear.
   - Enter numbers (1–8) to perform different operations.

---

## Instructions for Testing

You can test the system using the following steps:

### 1. Test Adding Rooms
- Choose option `1` (Add Room).
- Enter:
  - Room No: e.g., `A101`
  - Capacity: e.g., `3`
  - Gender: `M` or `F`
- Try:
  - Valid capacity (e.g., 3)
  - Invalid capacity (0 or negative) - should show error
  - Duplicate room number - should show “room already exist”

### 2. Test Adding Students
- Choose option `3` (Add Student).
- Enter:
  - ID: e.g., `S001`
  - Name: e.g., `Rohan`
  - Gender: `M` or `F`
  - Year: e.g., `1`
  - Course: e.g., `CSE`
- Try:
  - Valid year (1, 2, 3, 4)
  - Invalid year (0 or negative) - should show error
  - Duplicate student ID - should show “student already exists”

### 3. Test Viewing Data
- Use `2` (View Rooms) to verify rooms are added correctly.
- Use `4` (View Students) to verify students are added and see their room and allocation date after allocation.

### 4. Test Room Allocation
- Make sure at least one room and one student  exist.
- Choose option `5` (Allocate Room).
- Enter a valid student ID.
- Expected:
  - If a matching room with vacancy exists - “Succesfully Allocated”
  - Student gets `allocated_room` and `allocation_date` (current date).
  - If no suitable room exists - “Matching room not available.”

### 5. Test Room Deallocation
- After allocation, choose option `6` (Deallocate Room).
- Enter the same student ID.
- Expected:
  - Student is removed from room’s `occupants`.
  - `allocated_room` and `allocation_date` become `None`.
  - If student is already not allocated → shows proper message.

### 6. Test Clear All Data
- Choose option `8` (Clear All Data).
- Confirm with `yes` (or `y` as per your code).
- After this:
  - `2` (View Rooms) - should show “No Rooms Found”
  - `4` (View Students) - should show “No Students Found”

### 7. Test Exit
- Choose option `7` to exit the application.




