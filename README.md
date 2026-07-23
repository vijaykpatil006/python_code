# python_code
generating random password as per user requirement 
import random

lower_lenth=int(input("Enter the Lower digit"))
uper_lenth=int(input("Enter the uper digit"))
digit_lenth=int(input("Enter the digit"))
symbol_lenth=int(input("Enter the symbol"))


lower = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
upper = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'Y', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
digits = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '"', '#', '$', '%', '&', "'", '(', ')', '*', '+', ',', '-', '.', '/', ':', ';', '<', '=', '>', '?', '@', '[', '\\', ']', '^', '_', '`', '{', '|', '}', '~']

password_list=[]

# getting Random alphabets
for i in range(lower_lenth):
    password_list.append(random.choice(lower))
    
#getting random up alphabets
for i in range(uper_lenth):
    password_list.append(random.choice(upper))    
    
   #getting random digits
for i in range(digit_lenth):
    password_list.append(random.choice(digits))  
    
       #getting random digits
for i in range(symbol_lenth):
    password_list.append(random.choice(symbols))  
    
    
final_password='' 

# converting list to string
    
random.shuffle(password_list)
final_password = "".join(password_list)

print("your password is here:", final_password)
