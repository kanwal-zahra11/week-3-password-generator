# Random Password Generator

A simple Python command-line tool that generates a secure, random password based on a length entered by the user.

## Features
- Asks the user for the desired password length (4–64 characters, 15+ recommended)
- Generates a random password using letters, numbers, and special characters
- Makes sure the password always has at least one letter, one number, and one symbol
- Calculates the password's entropy (in bits) and shows its strength rating (Very Weak to Very Strong)
- Uses Python's `secrets` module instead of `random` for cryptographically secure randomness

## Modules Used
- `secrets` – generates cryptographically secure random choices
- `string` – provides ready-made character sets (letters, digits, punctuation)
- `math` – used to calculate password entropy

## How to Run
```bash
python password_generator_student_symbols.py
```
Then enter the desired password length when prompted.

## Example Output
```
Enter password length (4-64, 15+ recommended by NIST): 16

Your generated password is: <&<TCV\HYF(8wM,B
Password length: 16
Entropy value: 104.9 bits
Password strength: Strong
```

## What I Learned
- How to work with Python's built-in `secrets` and `string` modules
- Why `secrets` is safer than `random` for generating passwords
- How password entropy is calculated and what it means for password strength
- Basic input validation to handle bad user input
