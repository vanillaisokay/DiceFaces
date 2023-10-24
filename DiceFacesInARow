'''
Created on Oct 23, 2023

@author: jer21551
'''
def introduction():
    print("Please enter the game version you want: ")
    print("  Enter [1] to trace the game.")
    print("  Enter [2] to skip and give the answer.")
    global choice
    choice = int(input("Please enter 1 or 2.\n"))

def startGame():
    global diceFace
    global numTimes
    diceFace = int(input("Please enter the dice face number that would you like to be repeated.\n"))
    numTimes = int(input(f"Please enter the number of times that you would like {diceFace} to appear in a row.\n"))

def traceResults(): #traces real time results, v1 exclusive        
    print(f"You rolled a {number}")
    print(f"Number of times rolled in a row: {i}")
    print(f"Number of throws: {numThrows}\n")

def rollDice(): #rolls the dice
    import random
    global number
    global numThrows
    global i
    i = numThrows = 0

    while (i != numTimes):
        number = random.randint(1,6)
        numThrows += 1
        if number == diceFace:
            i += 1
        else:
            i = 0
        if choice == 1: #v1 exclusive
            traceResults()
    print(f"  It took {numThrows} throws to roll the number {diceFace} to {numTimes} times in a row.\n")

#final output
while True:
    introduction()
    startGame()
    rollDice()
    while True:
        print(f"\tWould you like to play the game again?")
        userInput = input(f"\t    Enter [Y] for yes, [N] for no.\n")
        if userInput in ('y', 'n'):
            break
        print("Invalid input. Please enter [Y] or [N] and try again.")
    if userInput == 'y':
        continue
    else:
        print("Thank you for playing. See you next time!")
        break
