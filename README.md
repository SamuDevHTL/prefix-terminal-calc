# Prefix Terminal Calculator

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![macOS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0)

> A powerful terminal calculator with SI unit prefix support and automatic unit conversion

## 📋 Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Usage Examples](#usage-examples)
- [Unit Support](#unit-support)
- [Roadmap](#Roadmap)

## ✨ Features

### 🔢 Calculation Features
- Support for SI unit prefixes (p, n, µ, m, k, M, G, T)
- Automatic unit conversion and simplification
- Complex mathematical expressions
- Interactive mode and command-line arguments
- Ohm's law automatic calculations
- Unit-aware arithmetic operations

### 📐 Unit Handling
- Automatic unit simplification
- Support for common electrical units (V, A, Ω)
- Unit multiplication and division
- Unit power handling
- Unit alias support (e.g., 'ohm' → 'Ω')

### 🎯 Smart Features
- Intelligent prefix selection for output
- Automatic scientific notation for very small/large numbers
- Error handling for invalid expressions
- Support for parentheses in expressions
- Interactive mode with history

## 🛠️ Technologies Used
- Python 3.6+
- Regular expressions for parsing
- No external dependencies

## 🏗️ Project Structure

### Core Components
- `Quantity` class for unit handling
- Expression parser
- Tokenizer
- Interactive mode
- Command-line interface

### Key Functions
```python
def parse_quantity(token)      # Parse a single quantity with units
def tokenize_expr(expr)       # Break expression into tokens
def parse_expression(expr)    # Parse and evaluate full expression
def interactive()            # Run in interactive mode
```

## 🚀 Getting Started

1. Clone the repository
```bash
git clone https://github.com/your-username/prefix-terminal-calc.git
cd prefix-terminal-calc
```

2. Make the script executable
```bash
chmod +x calc
```

3. (Optional) Install globally
```bash
# Move to bin directory for global access
sudo mv calc /usr/local/bin/
# Now you can use 'calc' command from anywhere
```

4. Run the calculator
```bash
# Interactive mode
calc

# Command-line mode
calc "5kΩ * 2mA"
```

## 💡 Usage Examples

### Basic Calculations
```bash
>>> 5kΩ * 2mA
10V

>>> 10V / 2kΩ
5mA

>>> 1MΩ * 1µA
1V
```

### Complex Expressions
```bash
>>> (5kΩ + 3kΩ) * 2mA
16V

>>> 10V / (2kΩ + 3kΩ)
2mA
```

### Unit Prefixes
```bash
>>> 1MΩ
1MΩ

>>> 1µA * 1kΩ
1mV

>>> 1GΩ * 1nA
1V
```

## 📏 Unit Support

### Supported Units
- V (Volts)
- A (Amperes)
- Ω (Ohms)

### Supported Prefixes
| Prefix | Value | Example |
|--------|-------|---------|
| p      | 10⁻¹² | pA      |
| n      | 10⁻⁹  | nA      |
| µ      | 10⁻⁶  | µA      |
| m      | 10⁻³  | mA      |
| (none) | 10⁰   | A       |
| k      | 10³   | kA      |
| M      | 10⁶   | MA      |
| G      | 10⁹   | GA      |
| T      | 10¹²  | TA      |

## 🗺️Roadmap
- add complex calculations like sqrt, sin, cos, log ...
