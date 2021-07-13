# Number-Skip-game

import time
import random


print("I am going to count from 1 to 20, skipping a number. Can you figure out what number I skipped? We will play 5 times.")

score=0
for rep in range(5):
  number_to_skip=random.randint(3,18)
  print('Ready...')
  time.sleep(0.5)
  print('Set...')
  time.sleep(0.5)
  print('Go!')
  for i in range(1,21):
    if i==number_to_skip:
      continue
    print(i,end='\r')
    time.sleep(0.25)
    
  num=input("What number did I skip?")
  if num==str(number_to_skip):
    print("That is correct!")
    score+=1
  else:
    print(f"Wrong. I skipped {number_to_skip}")
    
print(f'Your score is {score} out of 5.')
