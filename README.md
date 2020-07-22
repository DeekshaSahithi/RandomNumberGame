# RandomNumberGame
import random
number = random.randint(1, 9)
print("Welcome to Guess Game!!")
guess= int(input('Enter Your Guess Number between 1 and 9:'))
try:
    while guess>9 or guess<1:
        print("enter the number between 1 and 9")
        guess = int(input("enter your number:"))
    while guess != number:
        print('Your Guess is WRONG!')
        if guess > number:
            print('Guessed number is Too High')
        elif guess < number:
            print('Guessed number is too Low')
        guess =int(input('Enter Your Guess Number between 1 and 9:'))
    if guess == number:
            print('your Guess is Correct!','Game completed')
except ValueError:
    string=str(guess)
    if str == 'exit':
        print('You Have Successfully exit from the game')
    else:
        print('Enter the valid number')
