# phonebook-management

📒 Phonebook Management System (C++ - Console Based)

A console-based Phonebook Management System implemented in C++ with support for both Admin and User roles.
The program allows adding, editing, searching, deleting, and listing phonebook contacts with an interactive console UI using Windows API (gotoxy, colors, borders, cursor movement).

✨ Features
🔐 Login System

Admin Login

Username: admin

Password: password

Full permissions.

User Login

Username: user

No password required.

Can only search contacts.

🔧 Admin Features

Admins have full access:

Add New Contact

Edit Existing Contact

Search Contact

By name

By phone number

Delete Contact

Multi-Delete Contacts (Select multiple entries)

List All Contacts

Super Search

Supports partial matches

Phrase search

Works on both names and phone numbers

Save and Exit

Writes contacts to phone book.txt

👤 User Features

Users have restricted access:

Search contact by name or phone number.

View contact details.

📁 Data Storage

All contacts are stored in phone book.txt

Format (4 lines per contact):

first_name
last_name_or_'-'
phone_number
email


On startup, the program reads all existing contacts and loads them into:

map1 → First name index

map2 → Last name index

map3 → Phone number index

map4, map5, map6 → Used for search operations

🖥️ Console Interface

The interface uses:

Windows API (windows.h)

Custom gotoxy() for cursor positioning

Color output using SetConsoleTextAttribute

Box-drawing borders

Smooth navigation using arrow keys, Enter, Backspace, etc.

⚠️ This program works only on Windows due to console APIs.

📦 Requirements

Windows OS

A C++ compiler with Windows API support
Example:

MinGW (g++)

MSVC (Visual Studio)

Dev-C++

CodeBlocks

▶️ Running the program

Compile using g++:

g++ main.cpp -o phonebook.exe


Run:

phonebook.exe

📚 Code Structure
Main Components

login()

border(), gotoxy() → UI functions

Person class:

add()

deletephoneno()

changedetails()

draw_fill()

supersearch()

recoverformfile()

writeinfile()

Searching and validation functions

Maps Used

map1 → First names

map2 → Last names

map3 → Phone numbers

map4, map5, map6 → Temporary search maps

🛠️ Internal Features

Supports tokenized search

Detects partial matches in super search

Handles multiple identical names

Navigable multi-delete selection

Automatically updates all maps during add/edit/delete

Ensures no duplicate phone numbers

💾 Saving Contacts

Contacts are automatically written to phone book.txt when:

Admin selects Exit

Program terminates properly
