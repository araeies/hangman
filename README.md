# hangman
hangman game

import random
 
word = ("EVAPORATE")
print ("guess the characters")
guesses = ''

while True:
  failed = 0
  for char in word:
    if char in guesses:
      print(char)
    else:
      print("_")
    failed +=1
    
    if failed == 0:
      print("you win")
      print("the word is: ", word)
      break
    
  guess = input("guess a character: ")
  if guess in guesses:
    print("you have already guessed this letter")
    
  guesses += guess
  
  if guess not in word:
    print("wrong")
  
    
