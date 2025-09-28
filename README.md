# Python Command-Line Calculator

A robust command-line calculator application built in Python. This project demonstrates best practices in software development, including a REPL interface, Object-Oriented Programming (OOP), input validation, comprehensive testing with pytest, and a CI/CD pipeline using GitHub Actions.

---

## ✨ Features

- **REPL Interface**: A Read-Eval-Print Loop for continuous user interaction.  
- **Object-Oriented**: Utilizes a factory pattern and dedicated classes for each calculation, promoting modularity and extensibility.  
- **Arithmetic Operations**: Supports Addition, Subtraction, Multiplication, Division, Power, Modulo, and Square Root.  
- **Calculation History**: View all previous calculations from the current session using the `history` command.  
- **Input Validation**: Gracefully handles non-numeric inputs and invalid operation choices.  
- **Error Handling**: Handles division-by-zero errors and invalid inputs for square root and modulo operations.  
- **Well-Tested**: Achieves 100% test coverage with unit and parameterized tests.  
- **CI Integrated**: Uses GitHub Actions to automatically run tests and verify coverage on every push.  

---

## 📂 Project Structure

```bash
.
├── .github/
│   └── workflows/
│       └── tests.yml      # GitHub Actions workflow configuration
├── app/
│   ├── __init__.py
│   ├── calculation/
│   │   └── __init__.py    # Calculation classes and factory pattern
│   ├── calculator/
│   │   └── __init__.py    # Main application logic (REPL)
│   └── operation/
│       └── __init__.py    # Core arithmetic functions (Operation class)
├── tests/
│   ├── __init__.py
│   ├── conftest.py
│   ├── test_calculation.py
│   ├── test_calculator.py
│   └── test_operations.py
├── .coveragerc            # Coverage tool configuration
├── LICENSE                # MIT License file
├── main.py                # Main entry point for the application
├── pytest.ini             # Pytest configuration file
└── requirements.txt       # Project dependencies
```

---

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

- **Python 3.8+**: Make sure Python is installed and accessible from your command line.  
  👉 [Download Python](https://www.python.org/downloads/)  

- **Git**: You'll need Git to clone the repository.  
  👉 [Download Git](https://git-scm.com/downloads)  

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
cd YOUR_REPOSITORY_NAME
```
### 2. Create and Activate a Virtual Environment

It is highly recommended to use a virtual environment to manage project dependencies.
```bash
# Create the virtual environment (e.g., named 'venv')
python3 -m venv venv
```

Activate it:

- macOS/Linux/WSL:
```bash
source venv/bin/activate
```

- Windows (PowerShell):
```bash
venv\Scripts\Activate.ps1
```

When active, you will see (venv) at the beginning of your terminal prompt.

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

---
## ▶️ How to Run the Application

With your virtual environment active, run the application from the project’s root directory:
```bash
python main.py
```

The application will start, and you can follow the on-screen prompts to perform calculations.

---
## Usage

Enter commands in the format:
```bash
<operation> <number1> <number2>
```
Supported Operations

- add: Adds two numbers.
- subtract: Subtracts the second number from the first.
- multiply: Multiplies two numbers.
- divide: Divides the first number by the second.
- modulo: Calculates the remainder of the first number divided by the second.
- square_root: Calculates the square root of the first number (the second number is ignored but required).

Special Commands

- help: Display the help message.
- history: Show the history of calculations for the current session.
- exit: Exit the calculator.

## Examples
```bash
>> add 10 5
Result: AddCalculation: 10.0 Add 5.0 = 15.0

>> subtract 15.5 3.2
Result: SubtractCalculation: 15.5 Subtract 3.2 = 12.3

>> modulo 10 3
Result: ModuloCalculation: 10.0 Modulo 3.0 = 1.0

>> square_root 9 0
Result: SquareRootCalculation: 9.0 SquareRoot 0.0 = 3.0

>> history
Calculation History:
1. AddCalculation: 10.0 Add 5.0 = 15.0
2. SubtractCalculation: 15.5 Subtract 3.2 = 12.3
3. ModuloCalculation: 10.0 Modulo 3.0 = 1.0
```

---
## ✅ Running Tests

This project uses pytest and pytest-cov for testing, with configurations managed in pytest.ini and .coveragerc.
The Continuous Integration pipeline requires 100% test coverage to pass.

- Run All Tests
```bash
pytest
```

- Run Tests with Coverage Check
```bash
pytest --cov=app --cov-fail-under=100
```
---

## 📄 License

This project is licensed under the MIT License.