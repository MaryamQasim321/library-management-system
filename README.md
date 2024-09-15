# Library Management System in C

This is a simple Library Management System written in C. It allows users to add, delete, search, update, view, and issue books in a library using file handling for data storage.

## Features
- **Add a Book**: Add a new book record to the system.
- **Delete a Book**: Remove a book record by copying all records except the one to be deleted into a new file.
- **Search for Books**: Search for books by ISBN, name, or author.
- **Update a Book**: Modify book details with a given serial number.
- **View All Books**: View all book records in a tabular form.
- **Issue a Book**: Mark a book as issued (reserved).
  
## File Structure

```c
FILE* book_data; // Global File pointer for handling book data file

void create_file();            // Create file in write or append mode
void header(char *status);      // Display a header showing the status of the current action
void menu();                    // Display the main menu
void add();                     // Add a new book record
void deleteRecord();            // Delete an existing book record
void search();                  // Search for a book by ISBN, name, or author
void update();                  // Update the details of an existing book
void view();                    // Display all book records in a formatted table
void issue();                   // Issue a book (mark as reserved)
void take_input(struct book* record); // Take input from user for a new book record
void print_single_record(struct book record); // Print details of a single book record
Usage
Clone the repository:


git clone https://github.com/your-username/library-management-system.git
Navigate into the project directory:



cd library-management-system
Compile the program using GCC:

gcc main.c -o library_management
Run the program:

./library_management


Program Flow
Main Menu: After starting the program, the user will be presented with a main menu with options to add, delete, search, update, issue, or view book records.
Adding Records: The user can add book details including title, author, ISBN, and reserved status.
Deleting Records: The user can delete a book by providing its serial number.
Searching for Books: The system allows searching based on various fields such as ISBN, name, or author.
Updating Records: The user can update book information.
Viewing All Records: Displays all books in a formatted table.
Issuing Books: Marks the selected book as issued (changes reserved status to "Yes").
Book Structure
Each book record is stored with the following structure:


struct book {
    int serial_no;
    char title[50];
    char author[50];
    char ISBN[20];
    char reserved[5];  // "Yes" or "No"
};


How It Works
The system uses file handling to store book records in a file (e.g., books.txt). All operations, such as adding, deleting, updating, and viewing books, are performed on this file. The global file pointer book_data is used to manipulate the book records.

Future Improvements
Add user authentication for borrowing books.
Improve search functionality with additional filters.
Add the ability to categorize books into genres or sections.
