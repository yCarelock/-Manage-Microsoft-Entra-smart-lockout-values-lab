# -Secure Password Generator in Python
<b-> Overview

A strong password is one of the cornerstones of cybersecurity. This project uses Python’s built‑in modules to generate a secure password composed of letters, digits, and punctuation. We’ll use the secrets module instead of the typical random module because it provides functions that are more appropriate for security-sensitive applications.
Step-by-Step Instructions
1. Prepare Your Environment
Install Python: Ensure you have Python 3.x installed. You can download it from python.org.

Editor Choice: Open your favorite text editor or IDE (for example, Visual Studio Code, Sublime Text, or even a simple text editor).

2. Create the Python Script
File Creation: Create a new file named password_generator.py.

3. Write the Code
Copy and paste the following code into your file:
import secrets
import string

def generate_password(length=12):
    """
    Generate a secure password using letters, digits, and punctuation.
    
    Parameters:
        length (int): Length of the generated password.
        
    Returns:
        str: A secure random password.
    """
    # Create a pool of characters: uppercase, lowercase, digits, and punctuation
    characters = string.ascii_letters + string.digits + string.punctuation
    
    # Securely choose random characters from the pool
    secure_password = ''.join(secrets.choice(characters) for _ in range(length))
    return secure_password

if __name__ == "__main__":
    # You can modify the password length as desired
    password_length = 12  
    print("Your secure password is:", generate_password(password_length))
Code Explanation:

Imports:

secrets: Provides secure random number generation.

string: Provides convenient string constants.

generate_password Function:

Combines uppercase, lowercase letters, digits, and punctuation into one pool.

Uses a list comprehension with secrets.choice() to generate each character securely.

Main Block:

Sets the desired password length (default is 12).

Prints the generated password to the console.

4. Run Your Script
Open your terminal or command prompt.

Navigate to the directory containing password_generator.py.

Run the script by typing: python password_generator.py

Here's the output I got
![2025-04-09 20_31_11-password_generator py - Visual Studio Code](https://github.com/user-attachments/assets/122698b6-1404-4fe0-a504-7a59b80aff59)
Every time you run the script, a new secure, random password will be generated.
