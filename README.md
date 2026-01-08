# Information System

This project is a console-based C++ application designed to manage student records efficiently. It serves as a simple database system that allows users to Create, Read, Update, and Delete (CRUD) student information, with data persistence handled through local text files.

The system features a menu-driven interface, making it easy to navigate through various functions such as adding new students, searching for specific records, and modifying existing data.

## Features

* **Add Records:** Capture student details including Last Name, First Name, Middle Initial, Age, and Gender.
* **View Database:** Display all stored student records in a formatted, tabular view.
* **Search Functionality:** specific students by any attribute (e.g., Search by Age, Last Name, etc.).
* **Edit Records:** Modify specific details of an existing student record found via search.
* **Delete Records:** Remove obsolete or incorrect student entries from the system.
* **Sorting:** Organize the student list alphabetically or numerically based on selected categories.
* **Persistent Storage:** Automatically saves data into separate `.txt` files (`lname.txt`, `age.txt`, etc.), ensuring data is not lost when the program closes.

## How It Works

The program utilizes the C++ Standard Library (`<list>`, `<fstream>`, `<string>`, `<algorithm>`) to handle data management.

1.  **Data Structure:** It uses a `struct info` to hold temporary student data in memory using linked lists (`std::list`).
2.  **File Handling:** Data is stored in a column-based text file format. There are five separate text files corresponding to specific fields (e.g., `lname.txt` stores all last names).
3.  **Interface:** The application uses a nested `switch-case` menu system to guide the user from the Start screen to the Home dashboard and subsequent operations.

## Getting Started

### Prerequisites

* **C++ Compiler:** GCC (MinGW), Clang, or MSVC.
* **Operating System:** Windows is recommended (due to the use of `system("cls")`).
    * *Note for Linux/macOS users:* You may need to change `system("cls")` to `system("clear")` in the source code before compiling.

### Installation

1.  **Download the Source Code**
    Save the C++ file (e.g., `main.cpp`) to your local machine.

2.  **Compile the Program**
    Open your terminal or command prompt and navigate to the directory containing the file. Run the following command:
    ```bash
    g++ main.cpp -o student_system
    ```

3.  **Run the Application**
    Execute the compiled program:
    ```bash
    student_system.exe
    ```

## Usage

1.  **Start the System**
    Upon launching, select **[a] Start** to load the Home menu.

2.  **Add a Student**
    * From the Home menu, select **[a] Add**.
    * Enter the required details (Name, Age, Gender).
    * The data is automatically appended to the text files.

3.  **View and Manage Data**
    * Select **[b] View** from the Home menu to see the table of students.
    * From the View menu, you can access the **Search** or **Sort** sub-menus.

4.  **Search, Edit, and Delete**
    * Navigate to the Search menu.
    * Choose a category (e.g., First Name).
    * Type the query.
    * Once a match is found, you can choose to **[a] Edit** or **[b] Delete** that specific record.

## File Structure

The program will automatically generate or update the following files in the same directory as the executable:

* `lname.txt`
* `fname.txt`
* `mname.txt`
* `age.txt`
* `gender.txt`

> **Note:** Do not manually alter the row count in these text files, as the program relies on line-by-line synchronization across files to read data correctly.
