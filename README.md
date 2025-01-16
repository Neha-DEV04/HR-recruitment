# HR Management System

## Overview
The HR Management System is a simple implementation of an Employee Management System using C. It allows the user to manage employee records in a Binary Search Tree (BST), ensuring efficient storage, retrieval, and updates. The program provides functionalities like adding, searching, updating, and deleting employee records.

---

## Features

1. **Load Employee Records from File**
   - Reads employee details from a file (`data.txt`) and populates the BST.

2. **Add New Employee**
   - Allows users to insert new employee details.
   - Prevents duplicate entries based on employee ID or name.

3. **View All Employee Details**
   - Displays all employee records in ascending order by name using in-order traversal of the BST.

4. **Search Employee**
   - Search by:
     - Employee Name
     - Employee ID
     - Designation

5. **Update Employee Details**
   - Increment employee's position (designation) and update salary.

6. **Delete Employee Record**
   - Removes an employee based on their ID and adjusts the BST accordingly.

7. **Password Protection**
   - Provides three levels of access:
     - Vice President (`2021`)
     - Administrator (`2022`)
     - Manager (`2023`)
   - Allows three attempts to enter the correct passcode.

---

## File Structure

### **Source Code:**
- `main.c` : Contains the implementation of the HR Management System.

### **Data File:**
- `data.txt` : Stores the employee records in the following format:
  ```
  <Number of Employees>
  <Name> <ID> <Gender> <Designation> <Email-ID> <Salary> <Leaves> <Blood Group> <Phone Number>
  ```
  Example:
  ```
  2
  Alice E001 Female Manager alice@mail.com 50000 0 O+ 9876543210
  Bob E002 Male Developer bob@mail.com 40000 0 A- 8765432109
  ```

---

## How to Run

1. **Compile the Code:**
   Use GCC or any other C compiler:
   ```
   gcc main.c -o hr_management
   ```

2. **Run the Program:**
   ```
   ./hr_management
   ```

3. **Ensure `data.txt` Exists:**
   Create a `data.txt` file with valid employee data before running the program.

---

## User Guide

1. **Login:**
   - Enter the correct passcode to gain access.
   - Passcodes:
     - Vice President: `2021`
     - Administrator: `2022`
     - Manager: `2023`

2. **Choose an Operation:**
   - Option Menu:
     1. View All Employees
     2. Add New Employee
     3. Search Employee
     4. Update Employee Details
     5. Delete Employee Record

3. **Follow On-Screen Prompts:**
   - Provide the required details as prompted.

---

## Functions in Detail

### 1. **Employee Management**
- **`insertfromfile`**:
  - Inserts employee details from the `data.txt` file into the BST.
- **`insertfromuser`**:
  - Allows users to add new employee details interactively.
- **`writeinfile`**:
  - Writes the current BST to the `data.txt` file.

### 2. **Search Functionalities**
- **`searchbyname`**:
  - Searches for an employee by their name.
- **`searchbyid`**:
  - Searches for an employee by their ID.
- **`searchbydesignation`**:
  - Searches for all employees with a specific designation.

### 3. **Update Employee Details**
- **`increment`**:
  - Updates an employee’s designation and salary based on their ID.

### 4. **Delete Employee**
- **`fireemployee`**:
  - Removes an employee from the BST.

### 5. **Utility Functions**
- **`count`**:
  - Counts the total number of employees in the BST.
- **`inorder`**:
  - Displays all employees in ascending order by name.

---

## Sample Output

### Login Screen:
```
************************************************************************************************************************************************************
								OFFICE MANAGEMENT SYSTEM

						ENTER PASSCODE = 2022
						Access Granted!

								WELCOME Mr. ADMINISTRATOR
```

### Main Menu:
```
------------------------------------------------------------------------------------------------------------------------------------------------------------

				1. GET THE DETAILS OF ALL THE EMPLOYEES		2. INSERT A NEW EMPLOYEE DETAILS

		3. SEARCH AN EMPLOYEE       4. INCREMENT AN EMPLOYEE       5. FIRE AN EMPLOYEE

						PLEASE ENTER YOUR CHOICE (1-7) =
```

---

## Limitations

1. Does not handle file corruption or malformed data.
2. User interface could be improved for better usability.
3. BST operations might slow down for large datasets.
4. No data encryption or advanced security mechanisms.

---

## Future Enhancements

1. Use a balanced tree (e.g., AVL Tree) for better performance.
2. Add role-based access control for different passcodes.
3. Implement a graphical user interface (GUI).
4. Integrate database support (e.g., MySQL) for scalability.
5. Add more robust error handling and validation mechanisms.

---

## Credits
This project is a demonstration of basic data structures and file handling in C for educational purposes.

