

**Project 2: Extended Console Application - To-Do List**

**Goal:** Deepening knowledge of OOP, file handling, collections, and introduction to threads.

* **Description:** This project involves creating a more sophisticated console application for managing a list of tasks. Users will be able to **add new tasks** by providing a description, setting a priority level (e.g., High, Medium, Low), and specifying a due date. The application will also allow users to **mark tasks as completed**, helping them track their progress. A crucial feature of this application is the ability to **save the to-do list to a file** and **load it back** when the application is run again, ensuring data persistence. This project aims to build upon the foundational Java knowledge acquired in the first phase by introducing more advanced object-oriented concepts, file input/output operations, and more complex data structures.
* **Key Concepts to Learn/Apply:**
    * Advanced OOP:
        * Inheritance (e.g., different types of tasks if you want to expand).
        * Polymorphism.
        * Interfaces (e.g., `TaskRepository` defining save/load operations).
        * Abstract classes (optional).
    * Advanced collections: `HashMap` (e.g., for quick task lookup by ID), `Set`.
    * Date and time handling (`java.time` package - `LocalDate`, `LocalDateTime`).
    * File handling: Saving and reading data to a text file (e.g., CSV) or object serialization.
    * Exception handling (more advanced, e.g., custom exceptions).
    * Generic types (basics).
    * Streams (Java Streams API) for processing collections (e.g., filtering, sorting tasks).
    * (Optional) Basics of threads - e.g., saving to a file in a separate thread to avoid blocking the user interface (can be tricky in the console, but worth trying to understand the concept).
* **Requirements:**
    * Create a `Task` class (id, description, priority - e.g., enum, due date - `LocalDate`, status - e.g., enum `PENDING`/`DONE`).
    * Implement a `TaskRepository` interface with methods `save(Task task)`, `findById(long id)`, `findAll()`, `deleteById(long id)`, `update(Task task)`.
    * Create an implementation of `TaskRepository` that stores tasks in a `HashMap` (`InMemoryTaskRepository`).
    * Create a second implementation of `TaskRepository` that saves/loads tasks to/from a file (`FileTaskRepository`).
    * Use `java.time` for handling deadlines.
    * Use the Stream API to filter (e.g., show incomplete tasks) and sort (e.g., by priority, due date) tasks.
    * Implement an enhanced console menu.
    * Implement robust error handling (e.g., what if the file does not exist, date parsing errors).
    * Project in Maven with dependencies (JUnit, optionally a CSV library like OpenCSV if you choose that format).
    * Write comprehensive unit tests for business logic and repositories (you can use Mockito to mock dependencies in the future, but focus on JUnit for now).
* **Technologies:** Java SE, Maven, JUnit, (Optional: OpenCSV).
* **Possible Future Enhancements:**
    * **Task Categorization:** Allow users to categorize tasks (e.g., personal, work, shopping).
    * **Reminders/Notifications:** Implement a system to remind users about upcoming deadlines (this would likely involve more advanced concepts like scheduling or integration with system notifications).
    * **Recurring Tasks:** Add the ability to create tasks that repeat on a regular basis (e.g., daily, weekly).
    * **Task Dependencies:** Allow users to define dependencies between tasks (e.g., task B cannot start until task A is completed).
    * **User Authentication:** If the application were to become multi-user, adding user authentication would be a key enhancement.
    * **Graphical User Interface (GUI):** Similar to the previous project, this console application could be evolved into a GUI application for improved usability.
    * **Integration with Cloud Storage:** Allow users to save and load their task lists from cloud storage services.
