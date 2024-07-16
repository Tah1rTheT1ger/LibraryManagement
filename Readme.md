# Online Library Management System (OLMS)
This project is an Online Library Management System (OLMS) implemented in C using socket programming. It consists of a server-side application and a client-side application that communicate over a network.

## Features

### Server-Side
- **File Locking:** Prevents race conditions during book borrowing or returning.
- **Concurrency:** Handles multiple clients simultaneously.
- **Password Authentication:** Ensures secure access.
- **User Management:** Supports adding, deleting, and modifying users.
- **Library Functions:** Allows adding, searching, deleting, and updating books, as well as viewing all books and members.

### Client-Side
- **Connect to Server:** Allows users to connect to the OLMS server.
- **Borrow and Return Books:** Facilitates borrowing and returning books.
- **View Books and Members:** Enables viewing all books and members.

## How to Run

### Prerequisites
- Ensure you have a Linux environment.
- Install the necessary development tools (e.g., `gcc`, `make`).

### Steps

1. **Compile the Applications:**
   Open your terminal in the project directory and run:
   make all

2. **Run the Server:**
   Start the server by executing:
   ./server

3. **Run the Client:**
   In a separate terminal window, start the client by executing:
   ./client

4. **To reset**
   Open your terminal in the project directory and run:
   make clean

## Server Functionality
The server listens for incoming client connections. Clients can perform the following actions:
- **Borrow Books:** Borrow books from the library.
- **Return Books:** Return borrowed books.
- **View All Books:** See a list of all available books.
- **View All Members:** See a list of all library members.

## Client Functionality
The client connects to the server and allows users to:
- **Login/Register:** Authenticate with the server.
- **Borrow Books:** Borrow books from the library.
- **Return Books:** Return borrowed books.
- **View All Books:** See a list of all available books.
- **View All Members:** See a list of all library members.

## Notes
- **File Locking:** The server uses file locking to ensure data consistency when multiple clients access the same book.
- **Socket Programming:** Both server and client use socket programming for network communication.
- **Concurrency:** The server handles multiple clients concurrently, ensuring a smooth user experience.

## Code Structure

### Server (`server.c`)
Handles incoming connections, authenticates users, and manages book borrowing and returning operations. It ensures data integrity using file locking and supports concurrent client handling.

### Client (`client.c`)
Connects to the server, sends requests for borrowing and returning books, and displays the results received from the server. It also allows users to view all books and members.