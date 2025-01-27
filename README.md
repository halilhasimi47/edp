# Library Management System

This project is a library management system that allows users to reserve books, manage overdue book notifications, and handle administrative tasks. The system uses an event-driven architecture to manage communication between different components.

## Files Overview

### 1. `app.py`
This file demonstrates a simplified flow of the library system. It initializes agents, registers event handlers, and processes user requests. Key operations include:
- User book reservation requests.
- Event queue processing to manage reservations and overdue alerts.

### 2. `events.py`
Defines the structure of events used within the system. Key classes include:
- **Event**: Base class for all events.
- **BookReservationRequestEvent**: Represents a user’s request to reserve a book.
- **ReservationConfirmationEvent**: Sent when a reservation is confirmed or denied.
- **OverdueBookAlertEvent**: Triggered for overdue books.
- **UserNotificationEvent**: Handles general notifications to users.

### 3. `handlers.py`
Contains the `EventHandler` class, which manages event-driven communication. Key features:
- Maintains a mapping of event names to their handlers.
- Emits events and invokes corresponding handler functions.

### 4. `main.py`
Serves as the primary entry point for running the system. It extends the functionality of `app.py` by:
- Adding an admin agent for library management.
- Demonstrating admin actions such as adding or removing books and approving or canceling reservations.
- Handling multiple event types, including user notifications and overdue alerts.

## Key Components

### Agents
- **User**: Represents library users who can request book reservations.
- **Library**: Manages book inventory and processes reservations.
- **NotificationSystem**: Sends notifications to users.
- **Admin**: Handles administrative tasks such as inventory management and reservation approval.

### Event Handling
The system employs an event-driven architecture. Events are created based on user actions or system processes and processed via registered handlers.
- Events are pushed to the `communication_queue`.
- The `EventHandler` processes these events and invokes appropriate handler functions.

### Example Workflow
1. Users request book reservations.
2. Requests are processed as events in the `communication_queue`.
3. Reservation confirmations or denials are handled and logged.
4. Overdue book alerts are generated and notified to users.
5. Admin actions (e.g., adding books, approving reservations) are executed.

## How to Run the System
1. Ensure all dependencies are installed.
2. Run the `main.py` script:
   ```bash
   python main.py
   ```
3. Follow the console output to observe user requests, event processing, and admin actions.

## Future Improvements
- Add a graphical user interface (GUI) for better interaction.
- Implement a persistent database for book and user information.
- Enhance the notification system to support email or SMS alerts.

## Conclusion
This project demonstrates a modular and extensible approach to building a library management system using Python. Its event-driven architecture allows for seamless interaction between components and efficient handling of user requests.



Medium Blog 

**Building a Smarter Library Management System with Python**

