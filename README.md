# Arithmetic Formatter

A Python project that arranges arithmetic problems vertically and side-by-side, with optional answer display.

## Overview

This project implements a function `arithmetic_arranger` that formats addition and subtraction problems for easy reading, following specific formatting rules. It handles up to five problems, validates input, and can display answers when requested.

## Features

- Formats addition and subtraction problems vertically.
- Supports up to 5 problems at a time.
- Validates input:
  - Ensures operators are `+` or `-`.
  - Checks that numbers contain only digits.
  - Limits numbers to four digits.
- Right-aligns numbers with proper spacing (single space between operator and longest operand).
- Adds dashes under each problem, matching its width.
- Optionally displays answers when `show_answers=True`.
- Returns error messages for invalid inputs.

## Installation

1. Ensure Python 3.x is installed on your system.
2. Download or clone this repository:
   ```bash
   git clone https://github.com/thesoulseizure/arithmetic-formatter.git
   ```
3. Navigate to the project directory:
   ```bash
   cd arithmetic-formatter
   ```

## Usage

1. Save the `arithmetic_formatter.py` file in your project directory.
2. Import and use the `arithmetic_arranger` function in a Python script or interpreter.

Example usage:

```python
# Basic formatting
print(arithmetic_arranger(["32 + 698", "3801 - 2", "45 + 43", "123 + 49"]))
```

Output:
```
   32      3801      45      123
+ 698    -    2    + 43    +  49
-----    ------    ----    -----
```

With answers:
```python
print(arithmetic_arranger(["32 + 8", "1 - 3801", "9999 + 9999", "523 - 49"], True))
```

Output:
```
  32         1      9999      523
+  8    - 3801    + 9999    -  49
----    ------    ------    -----
  40     -3800     19998      474
```

## Error Handling

The function returns error messages for:
- Too many problems (> 5): `"Error: Too many problems."`
- Invalid operators (not `+` or `-`): `"Error: Operator must be '+' or '-'."`
- Non-digit numbers: `"Error: Numbers must only contain digits."`
- Numbers exceeding four digits: `"Error: Numbers cannot be more than four digits."`
- Invalid problem format: `"Error: Invalid problem format."`

## File Structure

- `arithmetic_formatter.py`: Main Python script containing the `arithmetic_arranger` function.
- `README.md`: This documentation file.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make changes and commit (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.
