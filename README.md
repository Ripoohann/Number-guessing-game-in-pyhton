# Number-guessing-game-in-pyhton

import random

def guess_number(x):
    random_number = random.randint(1, x)
    guess = 0
    while guess != random_number:
        guess = int(input(f"Guess the number from 1 to {x: }"))
        if guess < random_number:
            print(f"Sorry your number <{guess}> is smaller than the correct number")

        elif(guess > random_number) :
            print(f"Sorry your number ({guess}) is larger than the correct number")
    print(f"YAYYYY!!, You have guessed the correct number: {random_number} ")

def computer_guess(x):
    low = 1
    high = x
    feedback=''
    while feedback != 'c' and low != high:
        guess = random.randint(low , high)
        feedback = input(f"Is {guess} too [high] or too [low] or is [correct] to your number").lower()
        if feedback == 'high':
            high = guess - 1
        elif (feedback == 'low'):
            low = guess + 1
    print(f"YAYYY!,The computer has guessed you number ({guess}) correctly")
