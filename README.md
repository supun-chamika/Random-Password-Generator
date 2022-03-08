# Random-Password-Generator
This is a random password generator created using python. This can generate any lenght of a password including upper and lower letters, digits and symbols and also it can save the generated password in txt file.

import models:
==========================
```
import random
import string
import os
```
get length of the password:
==========================
```
length = int(input("Enter the length of the password: "))
```
define character:
==========================
```
lower = string.ascii_lowercase
upper = string.ascii_uppercase
digit = string.digits
symbol = string.punctuation
```
combine characters:
==========================
```
collection = lower + upper + digit + symbol
```
create list of characters:
==========================
```
temp = random.sample(collection, length)
```
create password:
==========================
```
password = "".join(temp)
```
show the generated password:
==========================
```
print("Your Password is: ", password)
```
get response from user to save the password:
==========================
```
save = input('Do you want to save the password(yes/no): ')
```
get name of the password:
==========================
```
password_name = input('Enter the name of the password: ')
```
saving password in txt file:
==========================
```
if save == 'yes' or 'y' or 'Y':
    f = open(r"password.txt", "a")
    f.write(password_name+': '+password + '\n')
    f.close()
```
get the current directory:
==========================
```
directory = os.getcwd()
```
print txt file directory:
==========================
```
print('password saved in: \n' + directory + '\password.txt')
```
