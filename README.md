import random
print("Welcome to Guess Game!!")
guess = int(input('Enter Your Guess Number between 1 and 9:'))

try:
    def guessGame(num,gu):
      if num==gu:
        print('Your Guess is CORRECT!')
        guess=int(input('Try Again! Enter Your Guess Number between 1 and 9:'))
        return guess
      else:
         print('Your Guess is WRONG!')
         if gu > num:
            print('Guessed number is Too High')
         elif gu < num:
            print('Guessed number is too Low')
         guess=int(input('Try Again! Enter Your Guess Number between 1 and 9:'))
         return guess    
    while guess > 0 and guess<10:
        number=random.randint(1, 9)
        guess=guessGame(number,guess)
except ValueError:
    if guess=='exit':
        print('You Have Successfully exit from the game')
    else:
        print('Enter the valid input')        
