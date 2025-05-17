

# Phonebook Management System

## Description

**Phonebook Management System** is a C-based console application that allows users to manage contact information. It provides a simple and user-friendly interface for adding, searching, modifying, deleting, and listing contacts. Each contact stores personal information including name, address, phone number, email, and father's name. Data is saved using file handling for persistence across sessions.

---

## Features

### Contact Management

* **Add New Contact**
  Add a new contact with name, address, father's name, phone number, and email.

* **List All Contacts**
  View all contacts saved in the phonebook.

* **Search Contact**
  Search for a contact by name and view detailed information.

* **Modify Contact**
  Update contact details by searching for a contact's name.

* **Delete Contact**
  Remove a contact by name from the phonebook.

###  Additional Functionalities

* Menu-based navigation with `getch()` for smooth user interaction
* Formatted console output using `got()` function for manual character input
* Persistent data storage using binary file I/O (`fopen`, `fwrite`, `fread`)
* Displays informative prompts and error handling for better UX

---

##  Technologies Used

| Category           | Details                                                   |
| ------------------ | --------------------------------------------------------- |
| **Language**       | C                                                         |
| **Compiler**       | Turbo C / GCC                                             |
| **Libraries Used** | `stdio.h`, `conio.h`, `stdlib.h`, `string.h`, `windows.h` |
| **Data Storage**   | File Handling with `fopen()`                              |
| **UI**             | Text-based, Console Interface                             |

---

##  File Structure

* **`project`** (Binary File): Stores serialized contact records.
* **`temp.txt`** (Temp File): Used during deletion/modification for safe file rewriting.

---

## Structure of `person`

```c
struct person {
    char name[35];
    char address[50];
    char father_name[35];
    long int mble_no;
    char mail[100];
};
```

---

##  Data Flow

1. User selects an option from the menu.
2. Appropriate function (`addrecord`, `listrecord`, `modifyrecord`, etc.) is invoked.
3. Data is read/written using binary file handling.
4. UI updates based on user actions and results.

---

##  How to Run

1. Compile the program using a C compiler like GCC:

   ```bash
   gcc phonebook.c -o phonebook
   ```
2. Run the executable:

   ```bash
   ./phonebook
   ```
3. Use number keys (1–6) to navigate through the menu.

---

##  Limitations

* Data is not encrypted — for educational use only.
* Contact uniqueness is based only on the `name` field.
* No input validation for email or phone format.
* UI is console-based; not cross-platform GUI.

---

##  Future Improvements

* Add date-of-birth or group categories.
* Input validation for emails and phone numbers.
* Transition to a database-backed system (e.g., SQLite).
* Replace `conio.h` usage for better cross-platform compatibility.

---

##  Sample Menu Display

```
********WELCOME TO PHONEBOOK***********

          MENU
  1.Add New     2.List     3.Exit
  4.Modify      5.Search   6.Delete
```

