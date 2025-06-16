# AirBnB Clone - The Console

## Description

Welcome to the **AirBnB Clone Project**. This is the first phase of building a full-featured AirBnB web application. The goal of this stage is to create a command-line interpreter that will manage the objects of our application: creating, showing, updating, and destroying instances of classes.

The console provides an environment where users can interact with the system through commands. It supports both **interactive** and **non-interactive** modes and can handle different object types like `BaseModel`, `User`, `Place`, `State`, `City`, `Amenity`, and `Review`.

---

## Features

- **Interactive Console**: Accepts commands in a prompt (`(hbnb)`).
- **Non-Interactive Mode**: Accepts piped input and executes commands.
- **CRUD Operations**: Create, retrieve, update, and delete model instances.
- **Custom Command Parsing**: Advanced command interpretation for models.
- **Python OOP Structure**: Modular code with well-documented classes and functions.
- **Unit Testing**: Comprehensive test suite using `unittest`.
- **PEP8 Compliant**: Clean and readable Python code.

---

## How to Start the Console

First, make sure you have Python 3.8+ installed on Ubuntu 20.04.

```bash
git clone https://github.com/YOUR_USERNAME/alu-AirBnB_clone.git
cd alu-AirBnB_clone
chmod +x console.py
./console.py
```

---

## Usage Examples

### Interactive Mode

```bash
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) create BaseModel
(hbnb) show BaseModel 1234-5678-9012
(hbnb) update BaseModel 1234-5678-9012 name "My_Model"
(hbnb) destroy BaseModel 1234-5678-9012
(hbnb) quit
```

### Non-Interactive Mode

```bash
$ echo "create User" | ./console.py
$ echo "show User 1234-5678-9012" | ./console.py
$ cat commands.txt | ./console.py
```

---

## Technologies Used

- Python 3.8.5
- Ubuntu 20.04 LTS
- `unittest` module for testing
- `pycodestyle` for code formatting

---

## Repository Structure

```
alu-AirBnB_clone/
├── console.py                # Entry point of the command interpreter
├── models/                   # Contains model classes and engine
│   ├── base_model.py
│   ├── user.py
│   ├── amenity.py
│   ├── city.py
│   ├── place.py
│   ├── review.py
│   ├── state.py
│   ├── engine/
│   │   └── file_storage.py
│   └── __init__.py
├── tests/                    # Unit tests for each module
│   └── test_models/
│       └── test_base_model.py
├── README.md                 # Project documentation
├── AUTHORS                   # List of contributors
└── __init__.py
```

---

## Running Tests

To run all unit tests:

```bash
python3 -m unittest discover tests
```

To run a specific test file:

```bash
python3 -m unittest tests/test_models/test_base_model.py
```

You can also test in non-interactive mode:

```bash
echo "python3 -m unittest discover tests" | bash
```

---

## Supported Commands

- `create <class_name>` — Creates a new instance and prints its ID
- `show <class_name> <id>` — Displays the string representation of an instance
- `destroy <class_name> <id>` — Deletes an instance
- `all [class_name]` — Shows all instances, or those of a specified class
- `update <class_name> <id> <attr_name> <attr_value>` — Updates an instance
- `quit` or `EOF` — Exits the console
- `help` — Displays help information

---

## Contribution Guide

To contribute to this project:

1. Fork the repository  
2. Create a new branch  
3. Make your changes with clear documentation  
4. Write or update unit tests  
5. Push your branch and submit a pull request

---

## License

This project is licensed under the MIT License.

---

## Authors

See the `AUTHORS` file for the list of contributors.

---

