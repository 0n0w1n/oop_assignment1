# Project overview
 This project is a OOP Library Management System. It uses classes like Book, Member, and Library to manage book catalog, registered users, and track borrowing/returning transactions.

# Project Structure
##### There's 1 README file and 2 folders contain procedural and OOP style
    - procedural_version
        - library_procedural.py (Original code)
        - test_procedural.py (test code for procedural)
    - oop_solution
        - library_oop.py (OOP implement code)
        - test_oop.py (test code for OOP)

# Design Overview
- ## Book class
    ### Attribute
        - id (identifier for the book)
        - title (title of the book)
        - author (author of the book)
        - available_copies (current count of copies that are not checked out)
        - total_copies (fixed total number of copies the library owns)
    ### Key method
    - init (used to create a new Book object)
- ## Member class
    ### Attribute
        - id (identifier for the member)
        - name (member's name)
        - email (member's contact email)
        - borrowed_list (list used to store the IDs of the books the member currently has checked out)
    ### Key method
    - init (used to register a new Member object)
- ## Library class
    ### Attribute
        - books (list that stores all the Book objects in the library)
        - members (list that stores all the Member objects registered with the library)
        - borrowed_books (list of dictionaries tracking active borrowing transactions)
    ### Key method
    - add_book (creates a new Book object and adds it to the self.books list)
    - add_member (creates a new Member object and adds it to the self.members list)
    - find_book (iterates through self.books and returns the Book or None if not found)
    - find_member (iterates through self.members and returns the member or None if not found)
    - borrow_book (decrease book.available_copies, appends the book_id to member.borrowed_list, and logs the transaction in self.borrowed_books)
    - return_book (checks if the member borrowed the book. If True, it increase book.available_copies, removes the book_id from member.borrowed_list, and removes the transaction record from self.borrowed_books)
    - display_available_books (prints a list of all book titles that have at least one copy available)
    - display_member_books (prints the titles of all books currently held by a member)
# Testing
- ## Basic Operations
    - Adding books and members
    - Borrowing and returning books
    - Displaying information
- ## Edge Cases
    - Borrowing unavailable books
    - Exceeding borrowing limit
    - Returning books not borrowed
    - Non-existent books/members
- ## How to run your test code
        - run file test_procedural.py in procedural_version for test procedural version code
        - run file test_oop.py in oop_solution for test OOP style code
