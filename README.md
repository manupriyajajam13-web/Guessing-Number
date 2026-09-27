#Guessing Number
import random

lowest_number = 1
highest_number = 100
answer = random.randint(lowest_number,highest_number)
guesses = 0
is_running = True

print(f"Python Number Guaessing Game")
print(f"Select number between {lowest_number} and {highest_number}")

while is_running:
    guess = input("Enter a number: ")
    
    if guess.isdigit():
        guess = int(guess)
        guesses +=1
        if guess < lowest_number or guess > highest_number:
            print(f"Number is out of Range")
            print(f"Please Enter a valid number")
            guess = input("Enter a number: ")
        elif guess < answer:
            print(f"Number is TOO small")
        elif guess > answer:
            print(f"Number is TOO large")
        else:
            print(f"CORRECT")
            print(f"Number of Guesses are {guesses}")
            is_running = False
    else:
        print(f"Invalid Input")
