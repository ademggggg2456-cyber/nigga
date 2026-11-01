# nigga
fuck you
import random
import string
number = [1, 2, 3, 4, 5, 6, 7, 8, 9]
print("Welcome to the Passwords website:")
length_password = int(input("How long do you want your password to be? "))
letters_password = int(input("Enter the number of letters in the Passwords: "))
numbers_password = int(input("Enter the number of numbers in the Passwords: "))
symbols_password = int(input("Enter the number of symbols in the Passwords: "))
totals = letters_password + numbers_password + symbols_password
letters = random.choices(string.ascii_letters, k=letters_password)
symbols = random.choices(string.punctuation, k=symbols_password)
numbers = random.sample(number, k=numbers_password)
total = []
total.extend(letters)
total.extend(symbols)
total.extend(numbers)
random.shuffle(total)
password = ""
if totals != length_password:
    print("The length of the password is not equal to letters and numbers and symbols")
else:   
    for j in total:
        password += str (j)
print (password)
