# Snake-and-ladder
#Snake and ladder game with loops and random module 
import random  
def roll_dice(sides=6):
    return random.randint(1, sides)

snakes={38: 20, 45: 20, 51: 20, 65: 20, 91: 20, 97: 20}#in the form of {snake_head:snake_tail}

ladders={32: 50, 40: 50, 56: 50, 17: 50}
position=1
print(f' position ={position}' , '\n')
while True :
    status = input('wanna play ? , type no if u dont : \n ')
    if status=='no':
        print(f' position ={position}' , '\n')
        print(' Bye then ')
        break     
    step=roll_dice()
    
    if position+step in snakes :
        position =snakes[position+step]
    elif position+step in ladders:
        position= ladders[position+step]
        
    else:
         position+=step 
         
    print(f' position ={position}', '\n')
      
                                              