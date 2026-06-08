# Salary Tracker

A Python-based employee salary tracker that manages employee levels and salaries with built-in validation using property decorators. Built as part of the freeCodeCamp Python Certification.

## Features

- Tracks employee name, level, and salary
- Validates level promotions (no downgrading allowed)
- Enforces minimum salary per level
- Clean string representation with `__str__` and `__repr__`

## Levels & Base Salaries

| Level     | Base Salary |
|-----------|-------------|
| trainee   | $1,000      |
| junior    | $2,000      |
| mid-level | $3,000      |
| senior    | $4,000      |

## Project Structure

```
salary-tracker/
├── README.md
├── employee.py       # Employee class with property validators
└── main.py           # Demo usage
```

## Usage

```python
from employee import Employee

# Create a new employee
emp = Employee('Charlie Brown', 'trainee')
print(emp)                        # Charlie Brown: trainee
print(f'Base salary: ${emp.salary}')  # Base salary: $1000

# Promote employee
emp.level = 'junior'              # Updates level and salary automatically
```

## Validation Rules

- `name` must be a string
- `level` must be one of the four defined levels
- Promotion is one-directional — downgrading raises an error
- `salary` cannot be set below the base salary of the current level

## Requirements

- Python 3.6+
- No external dependencies

## Author
Ann Ahmad
