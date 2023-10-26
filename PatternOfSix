'''
Created on Oct 25, 2023

@author: jer21551
'''
def intro():
    print("\n\tThis game requests 6 dice numbers from the player.")
    print("\tThe game then throws the dice until that pattern appears.")
    print("\tThe game then tells the player how many throws it took.\n")

def startGame():
    print("\tPlease enter the six-number pattern you would")
    print("\tlike the computer to throw seperated by spaces.")
    global pattern
    pattern = [int(item) for item in input("").split()]

def rollDice():
    import random
    global dice1, dice2, dice3, dice4, dice5, dice6
    global match
    global throw
    throw = dice1 = dice2 = dice3 = dice4 = dice5 = dice6 = 0
    match = [dice1, dice2, dice3, dice4, dice5, dice6]
    while (pattern != match):
        throw += 1
        dice1 = random.randint(1,6)
        dice2 = random.randint(1,6)
        dice3 = random.randint(1,6)
        dice4 = random.randint(1,6)
        dice5 = random.randint(1,6)
        dice6 = random.randint(1,6)
        match = [dice1, dice2, dice3, dice4, dice5, dice6]
        #print(f"Attempt #{throw}")
        #print(match)
    print(f"\n\tIt took {throw:,} throws to get the pattern {' '.join(map(str,pattern))}\n")

intro()
while True:
    startGame()
    rollDice()
    while True:
        print(f"\t   Would you like to play the game again?")
        userInput = input(f"\t     Enter [Y] for yes, [N] for no.\n")
        if userInput in ('y', 'n'):
            break
        print("\tInvalid input. Please enter [Y] or [N] and try again.")
    if userInput == 'y':
        continue
    else:
        print("\tThank you for playing. See you next time!")
        break
