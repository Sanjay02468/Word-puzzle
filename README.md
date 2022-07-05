# Word-puzzle
import random

def choose():
  words = ['STRONG', 'DOCTOR', 'BACKSPACE', 'KEYBOARD', 'EXAMS', 'RAINBOW', 'PYTHON', 'VIRUS', 'FUNDAMENTALS', 'SOLUTION', 'SMILE', 'SMART', 'CRICKET', 'ANIME', 'BASKETBALL', 'VOLLEYBALL']
  pick=random.choice(words)
  return pick

def jumble(word):
  jumbledword="".join(random.sample(word, len(word)))
  return jumbledword

def thanks(P1Name,P2Name,pp1,pp2):
  print(P1Name, 'Your score is: ', pp1)
  print(P2Name, 'Your score is: ', pp2)
  print('Thankyou for playing')
  
def play():
 P1Name = input('HI! Player 1, Enter your name \n')
 P2Name = input('HI! Player 2, Enter your name \n') 
 pp1 = 0;pp1=int(pp1)
 pp2 = 0;pp2=int(pp2)
 turn = 0;turn=int(turn)
while(1):
   #computers task
   pickedword = choose()
   question = jumble(pickedword)
   print('\n', question)
   #player 1:
   if(turn%2== 0):
     print(P1Name, 'Your Turn to play')
     answer = input('what is the word i choose \n')
     if (answer == pickedword):
       pp1 = pp1+1
       print('your score is : ', pp1)
       n = int(input('Press 1 to continue or 0 to Quit:'))
       if(n==0):
         thanks(P1Name,P2Name,pp1,pp2)
         break
     else:
       print('you have still 2 more chances try your best.')
       answer = input('what is the word i choose \n')
       if (answer == pickedword):
         pp1 = pp1 + 1
         print('your score is : ', pp1)
         n = int(input('Press 1 to continue or 0 to Quit:'))
         if(n==0):
            thanks(P1Name,P2Name,pp1,pp2)
            break
       else:
         print('you have still 1 more chances try your best.')
         answer = input('what is the word i choose \n')
         if (answer == pickedword):
           pp1 = pp1 + 1
           print('your score is : ', pp1)
           n = int(input('Press 1 to continue or 0 to Quit:'))
           if(n==0):
             thanks(P1Name,P2Name,pp1,pp2)
             break
         else:
           print('your 3 chances are completed.')
           print('Better luck next time.')
           print('I thought the word:', pickedword)
           n = int(input('Press 1 to continue or 0 to Quit:'))
           if(n==0):
             thanks(P1Name,P2Name,pp1,pp2)
             break
    # player 2:
   else:
     print(P2Name, 'Your Turn to play')
     answer = input('what is the word i choose \n')
     if (answer == pickedword):
       pp2 = pp2 + 1
       print('your score is : ', pp2)
       n = int(input('Press 1 to continue or 0 to Quit:'))
       if(n==0):
         thanks(P1Name,P2Name,pp1,pp2)
         break
     else:
       print('you have still 2 more chances try your best.')
       answer = input('what is the word i choose \n')
       if (answer == pickedword):
         pp2 = pp2 + 1
         print('your score is : ', pp2)
         n = int(input('Press 1 to continue or 0 to Quit:'))
         if(n==0):
           thanks(P1Name,P2Name,pp1,pp2)
           break
       else:
         print('you have still 1 more chances try your best.')
         answer = input('what is the word i choose \n')
         if (answer == pickedword):
           pp2 = pp2 + 1
           print('your score is : ', pp2)
           n = int(input('Press 1 to continue or 0 to Quit:'))
           if(n==0):
             thanks(P1Name,P2Name,pp1,pp2)
             break
         else:
           print('your 3 chances are completed.')
           print('Better luck next time.')
           print('I thought the word:', pickedword)
           n = int(input('Press 1 to continue or 0 to Quit:'))
           if(n==0):
             thanks(P1Name,P2Name,pp1,pp2)
             break
   turn = turn + 1
     
play()
