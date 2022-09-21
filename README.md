# Cricket_game_Based_on_pythoncode
# A very Basic and Interesting Cricket Game that is based on python code for  Entertainment Where you can interact with code and That Give you as live Experience. 
import random
import time
print(" match instructions ->")
print(" * This a simple cricket game Thats will Definatly entertain you")
print(" * This a bowler based game To out the Batsman  you need to  guess a number, if you guess a number correctly the Batsman will be out, if not The score will be adding up to End of Overs or up to Last wickets i.e upto 10 wickets ")
print("I hope You will enjoy the game ")
print('-')#this is to give some space so that code will be easy read;
print('-')#This line is to give some space
print('-')

toss=random.randint(1,2)
print("Toss Time choose 1=heads,2=Tails")
user_choice=int(input("enter the number from 1 to 2:"))
if toss==user_choice:
    print("you won the toss!!! ")
else:
    print("opponent won the toss!!")
print('-')#this line is to give some space
print('-')
print('-')
time.sleep(2)



print("------------------Game Starts in------------------!!!")
c=10
while c>=0:
    print(c)
    time.sleep(1)
    c-=1
    
    
print()#This line is give some space so that it will be easy to read the code 


print("The Game started Here comes the First Ball---->>>")


print()#This line is give some space so that it will be easy to read the code 


runs=0
overs=0
balls=0
wickets=0
reviews=2
while balls<30:
    batsman=random.randint(1,6)
    score=random.randint(0,6)
    if score==6:
        print("SKY SHOT !!!  Thats!!! MAXIMUM gone for SiX!!! ^^|^^")                                                 
    elif score==4:
        print("boundry gone for FOUR----<<|>>----")
                             
    bowler=int(input("enter the number from o to 5:"))
    balls+=1
    if batsman>5:
        print("no ball!!!")
        runs=runs+1
        balls-=1
        
    
    if batsman==bowler:
        print("out ")
        if reviews!=0:
            
            choice_drs=str(input("Do u want to take review y/n:"))
            drs=random.randint(0,1)
    
            if choice_drs=="y":
                u_drs=int(input("enter a number 0 to 1 :"))
                if drs==u_drs:
                    print("Not out ")
                    print("Review retained reviews left=",reviews)
                elif drs!=u_drs:
                    print("out")
                    wickets+=1
                    reviews-=1
                    print("wickets=",wickets)
                    print("reviews left=",reviews)
                
            elif choice_drs=="n":
                print("out")
                wickets+=1
                
                print("wickets=",wickets)
                print("reviews left=",reviews)
            
                
            elif reviews==0:
                print("Reviews over")
                break
        
        else:
            wickets+=1   
        
            print("total wickets=",wickets)
    elif batsman!=bowler:
        print("score",score)
        runs=runs+score
       
      
        print("total runs=",runs)
        print("---------score Boad----------")
        print(runs,"/",wickets)
    if balls>30 :
        print("end of the innings")
        break
    if wickets>10:
        print("All out")
        print(" End of the innings")
        print("---------score Boad----------")
        print(runs,"/",wickets)
        print("Target =",runs+1)
    if balls%6==0:
        overs+=1
        print("///////////  end of the",overs,"over!!!   /////////")
        print("score Board=",runs,"/",wickets)
        
print("------------------- second innings-----------------")
