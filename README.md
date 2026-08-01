# Password Generator (Project 3)

This is a small Python project I made where the program creates a random password for you. You just tell it how long you want the password and it does the rest.

## What it does

- Asks you how long you want your password (anywhere from 4 to 64 characters, though 15+ is what's actually recommended for it to be secure)
- Randomly picks letters, numbers, and symbols to build the password
- Double checks the password has at least one letter, one number and one symbol in it, if not it just generates again
- At the end it also tells you the entropy of the password (basically a number that tells how hard it would be to guess/crack) and gives it a rating from Very Weak to Very Strong

## Modules I used

- `secrets` - this is what actually picks the random characters. I initially thought of using `random` but turns out that one isn't actually safe for passwords since it can be predicted, `secrets` is the proper one to use for this kind of stuff
- `string` - just has the letters/numbers/symbols already defined so I didn't have to type them all out manually
- `math` - used this for the entropy calculation (log2 stuff)

## How to run it

```bash
python password_generator_student_symbols.py
```

it'll just ask you for a length and print out the password after that.

## Example

```
Enter password length (4-64, 15+ recommended by NIST): 16

Your generated password is: <&<TCV\HYF(8wM,B
Password length: 16
Entropy value: 104.9 bits
Password strength: Strong
```

## Things I learned while doing this

Honestly before this I didn't even know `secrets` was a module, I would've just used `random` like normal. Learned why that's actually a bad idea for passwords/security stuff since random's numbers aren't "truly" random, they can be predicted if someone knows the seed.

