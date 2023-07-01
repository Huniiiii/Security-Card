# Security-Card

It is a security center. The security center only accepts Visa cards, MasterCard credit cards, American Express cards and Discover cards. The rest are invalid for the security center. We will collect the user's name, age, password and card number by inputting. For security, we will hide the password to prevent the password from being exposed after disclosure. Finally, we will write in a text file for all users.

Through a series of calculations, the user information will be written in the huni file (text file), which is convenient for customers who bought my code. The user can select several users to enter the name, age, password, and card number and infer whether the user is good or bad through the Issuer identification number method. Then write the users' information in the huni file(text file) (for privacy, all but the first three digits of the password must be *)

## Part1 

•	Create the text file, and the text file’s name should be called “information.txt”  

•	Create n using eval, and ask the user “How many users do you have:” (eval is int + float, which means if you use eval, you can input int and float, eval will automatically process. ###we have to make sure that all our code should be in the text file line. There needs to be one tab after the line   
With open(“huniTest.txt”, “w”) as Huni: " 

**For example:
with open(“huniTest.txt”, “w”) as Huni:
n = input(“Huni is a great leader”)
for I in range (n):
  print(“Huni is nice”)
  …..
  …..**

•	And create for loop which ranges n (how many users do you have: that one) 
We need this effect
![image](https://github.com/Huniiiii/Security-Card/assets/87155903/59908db7-b6a9-48a3-89ed-bf1869d163aa)

•	So, if we want to get this kind of effect, we need to print(f”---User{i+1}---")
•	And we want to get the user’s name, age and password (password we want to ask the user to enter at least 6 characters, whatever letters or numbers), like the above photo. 
•	In case we need to define, is the user enters at least six characters. (using a while loop or if depend on personal habit, I personal recommend to use while loop. Because we want to make sure that users input at least six characters, if not we want to ask again if we use for loop, can only be used a certain number of times. Using While True we can ask many times we want. And end it if the user's input meets the condition.)
•	Ask the user for the card number using print(cardNumber)

---------------------------------------------------------------------------------------

## Part2 
• Here, we want to use Allan’s file, the function name isValid(cardNumber), and we have to define whether is the user is good or not using the if statement. Furthermore, we need to use Kyse object called (GoodUser). For example, user = GoodUser(name, age, password, cardNumber). If the user is bad, we can do the same process as the user using else.
Finally, we want to write users’ information into information.txt. ###we have to make sure that all our code should be in the text file line. There needs to be one tab after the line   
 With open(“huniTest.txt”, “w”) as Huni: " 

![image](https://github.com/Huniiiii/Security-Card/assets/87155903/42b30f09-3b44-40fb-a109-f19b8cfde0fb)
 
**user.getName()
user.getAge()
user.getPassword()
user.getCardNumber()
user.status**

Create a file called checkValid.py
Number is the card number, we can check the code by entering your real card number. It will identify Visa cards, MasterCard credit cards, American Express cards and Discover cards

  1.	From left to right, we want odd numbers and multiply by 2. If doubling of digit results in a two-digit number, add up the two digits to get a single-digit number.
  
  2.	Add all single-digit numbers from last step
  
  3.	Add all digits in the odd places from right to left in the card number.
  
  4.	Sum the results from Steps 2 and 3.
  
  5.	If the result from Step 4 can be divisible by 10, the card number is valid, otherwise, it is invalid.

We are going to use the next function I listed
# Return true if the card number is valid
def isValid(number):
# Get the result from Step 2
def sumOfDoubleEvenPlace(number):
# Return this number if it is a single digit, otherwise, return
# the sum of the two digits
def getDigit(number):
# Return sum of odd place digits in number
def sumOfOddPlace(number):
# Return true if the digit d is a prefix for number
def prefixMatched(number, d):
# Return the number of digits in d
def getSize(d):
# Return the first k number of digits from number. If the
# number of digits in number is less than k, return number.
def getPrefix(number, k):

The condition is that cards have 13 and 16 digits, and cards all start with
•	4 for Visa cards
•	5 for MasterCard credit cards
•	37 for American Express cards
•	6 for Discover cards
https://gocardless.com/guides/posts/what-is-luhn-algorithm/
https://www.geeksforgeeks.org/luhn-algorithm/
https://www.validcreditcardnumber.com/

---------------------------------------------------------------------------------------
Part 3
To create a class called User
And create function __ init__ which contain name, age password, cardNumber
We need to encapsulation all the name, age, password and cardNumber
Because we encapsulate the name, age ,password and cardNumber, we also want to get those. 
Which means that we need to create the function getName, getAge, getPassword (we also want to hide the users’ password and we also show first 3 digits number other digits we want to hide using *) 
for example: self.__huniPassword [:3] + “*” * (len(self.__huniPassword) -3).
 
and getCardNumber. And we return those.

Create another class called GoodUser(User):
we want to use User class name, age, password, cardNumber. 
We need to use super(). And want to want self.status = “Valid” in the end of GoodUser class
same process for bad user we want to create class called BadUser(User):
We need to use super(). And want to want self.status = “Invalid” in the end of BadUser class


