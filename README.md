# Luhn Algorithm 🔐

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

A Python implementation of the Luhn Algorithm for validating credit card numbers and other identification numbers.

## 📜 About
The Luhn Algorithm is a simple checksum formula used to validate a variety of identification numbers, especially credit card numbers. This implementation helps developers verify the validity of such numbers in their applications, providing a foundation for understanding basic cryptographic validation techniques.

## ✨ Features
- Validate credit card numbers using the Luhn checksum
- Handle numbers with hyphens and spaces
- Simple command-line execution
- Easy integration into Python projects
- Clear validation feedback

## 🚀 Quick Start

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/fahadelahikhan/Luhn-Algorithm.git
   cd Luhn-Algorithm
   ```

2. Run the application:
   ```bash
   python Luhn-Algorithm.py
   ```

### Basic Usage
```python
# Import the validation function
from luhn import verify_card_number

# Test a valid card number
card_number = '4111-1111-4555-1141'
is_valid = verify_card_number(card_number)
print(f'Card is {"VALID" if is_valid else "INVALID"}')  # Output: VALID

# Test an invalid card number
invalid_card = '1234-5678-9012-3456'
is_valid = verify_card_number(invalid_card)
print(f'Card is {"VALID" if is_valid else "INVALID"}')  # Output: INVALID
```

### Example Validation
```python
# Validate a Discover card number
discover_card = '6011-1111-1111-1117'
validation_result = verify_card_number(discover_card)
print(validation_result)  # Output: True

# Validate an American Express number
amex_card = '3782-822463-10005'
validation_result = verify_card_number(amex_card)
print(validation_result)  # Output: True
```

## 📖 How It Works
The Luhn Algorithm works by:
1. Reversing the input number
2. Doubling every second digit
3. Summing the digits of these doubled values (if >=10, sum the individual digits)
4. Summing all the undoubled digits
5. Checking if the total modulo 10 is equal to 0

## ⚖️ License
Distributed under the MIT License. See [LICENSE](LICENSE) for details.

---

> **Note**: This implementation is for educational purposes and basic validation. For production use, consider additional security measures and validation checks beyond the Luhn Algorithm.
