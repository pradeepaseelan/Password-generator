#password generator sample program

import random
import string

def generate_password(length=12, use_digits=True, use_symbols=True):
    characters = string.ascii_letters  # a-z + A-Z

    if use_digits:
        characters += string.digits  # 0-9
    if use_symbols:
        characters += string.punctuation  # !@#$%^&*()_+ etc.

    password = ''.join(random.choice(characters) for _ in range(length))
    return password

# Example usage
print("Generated Password:", generate_password(length=16, use_digits=True, use_symbols=True))
