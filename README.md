# While-Loop-Example
While loop used in User Login System
# User Registration & Login System (Python)

This project is a basic **User Registration and Login System** made using Python.  
The goal is to demonstrate the use of **while loops**, **condition checking**, and **user input handling**.

---

## 🚀 Features

1. New user registration  
2. Username and password validation (cannot be empty)  
3. Login authentication using while loop  
4. Allows multiple login attempts until credentials are correct  

---

## 🧠 Logic Flow

### Registration Phase
- User must enter a username and password.
- If either field is empty, system asks again.
- Once valid credentials are entered, registration is successful.

### Login Phase
- User enters the username and password.
- If credentials match the registered values → Login successful.
- Otherwise → User is prompted again to enter correct credentials.

---

## 🧾 Code Example

```python
# Predefined variables
correct_username = ""
correct_password = ""

# Registration Process
print("---User Registration---")

while correct_username == "" or correct_password == "":
    new_user = input("Enter a new username: ")
    new_pass = input("Enter a new password: ")

    if new_user != "" and new_pass != "":
        correct_username = new_user
        correct_password = new_pass
        print("Congrats! Registration Successful")
    else:
        print("Username and password cannot be empty. Please try again.")

# Login Phase Starts
print("\n--- Login Phase Starts ---")

while True:
    login_user = input("Enter username: ")
    login_pass = input("Enter password: ")

    if login_user == correct_username and login_pass == correct_password:
        print("Login Successfully!")
        break
    else:
        print("Incorrect username or password. Try again!")
