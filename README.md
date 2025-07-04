lab 1
#Mausham Sigdel || 081BEL046

1.write a python code that deletes all the duplicate elements from the list and prints the unique elements.
 
list=[1,2,1,2,3,4,5,5,4,6,7]
print("The list without duplicates are:")
print(set(list))

2. Create a tuple of 10 integer. write a program to display the maximum and minimum number from tuple.
t = (10,20,30,40)
l = []
import random
for i in range(10):
	l.append(random.randint(1,101))
print(l)
t = tuple(l)
print(f"max value : {max(t)}")
print(f"min value : {min(t)}")


3.write a python program that accepts a list and returns a new list with only the even numbers from the original list.

original_list=[1,2,3,4,5,6,7,8,9,10]
new_list=[]
for i in original_list:
    if i%2==0:
        new_list.append(i)
print("The new list with only even numbers present is:")
print(new_list)

4.#write a program to count the number of each characters in a given string using a dictionary.

string="programming"
my_dict={}
unique_characters=set(string)
for ch in unique_characters:
    my_dict[ch]=string.count(ch)

print("Character frequency:")
for ch,count in my_dict.items():
    print(f"'{ch}':{count}")

5# create a set of prime numbers less than  50 . Write a program to check whether the given number exists in the set or not.

prime_numbers={2,3,5,7,11,13,17,19,23,29,31,37,41,43,47}
num=input("Enter the number you want to check \n")
number=int(num)
for i in prime_numbers:
    if number in prime_numbers:
        print("The given number exists in the set")
        break
    else:
        print("The given number doesnt exist in the set")    
        break

6.# Given two lists,write a program to find their intersection using sets

list1=[6,5,7,8,9]
list2=[8,9,10,11,12]
set1=set(list1)
set2=set(list2)
print("The intersection of the given sets is:\n")
print(set1.intersection(set2))

7.# write a program to merge two diictionaries and find the sum of the common keys

my_dict={'spandan':1,'ram':2,'shyam':3}
my_dict1={'spandan':5,'hari':6,'ramesh':7}
merged_dict=my_dict.copy()
merged_dict.update(my_dict1)
print("The merged dictionary is:")
print(merged_dict)
common_keys=set(my_dict.keys()).intersection(my_dict1.keys())
total_sum=0
for key in common_keys:
    total_sum+=(my_dict[key])+(my_dict1[key])
print(f"The sum of common keys is {total_sum}")    

8.#given a list of names,write a program to count how many times each name occurs using a dictionary

list=['spandan','aayush','ram','shyam','ram','shyam','aayush','spandan']
dict={}
unique_names=set(list)
for name in unique_names:
    dict[name]=list.count(name)

print("The number of times each name occured in the list is:\n")
for name,count in dict.items():
    print(f"{name}:{count}")  

9.write a python program to remove elements from a list that is also present in another list

list1=[1,2,'spandan','lochan',3,5,6]
list2=[4,5,'spandan',6]
revised_list=list(set(list1).difference(set(list2)))
print(revised_list)


10.
my_dict = {}
n = int(input("How many key-value pairs do you want to enter?\n"))

for i in range(n):
    key = input(f"Enter key {i+1}\n")
    value = input(f"Enter the value for the key 100{key}\n")
    my_dict[key] = value

print("Dictionary:\n", my_dict)

search = input("Search the key you want\n")
if search in my_dict:
    print(f"The value of the key '{search}' is:\n{my_dict[search]}")
else:
    print("Key not found.")



11. Python program to check wthether the given number is prime or not

number=int(input("Enter any number you want to check\n"))
count=0

if(number<0):
    print("Please,enter a positive number\n")
elif(number==1 or number==0):
    print("The number you entered is neither prime nor composite ")
else:    
    for i in range(1,number+1):
        if number%i==0:
            count+=1
        
if(count==2):
    print("The number you enetered is a prime number\n")
else:
    print("The number you enetered is not a prime number\n")   


12.# write a program that prints all even numbers between 1 to 100 using a loop

for i in range(2,100):
    if i%2==0:
        print(i)
13.# write a program that reads a number and prints the factorial of a number using a while loop

number=int(input("Enter the number whose factorial you want to find\n"))
fact=1
i=1
while(i<=number):
    fact=fact*i
    i=i+1

print(f"The factorial of {number} is {fact}")    

14.# write a program to print the multiplication table of a number using for loop

num = int(input("Enter the number to print its multiplication table: "))

print(f"\nMultiplication table for {num}:\n")
for i in range(1, 11):
    print(f"{num} x {i} = {num * i}")


15.# write a program to find the largest and the smallest number in the list entered by the user

user_input=input("Enter the elements of the list\n")
user_list=list(map(int,user_input.split()))
maximum=max(user_list)
minimum=min(user_list)
print(f"maximum={maximum} and minimum={minimum}")

16.# write a program that accepts 10 integers from the user and counts how many of them are positive , negative nd zero.
total_count=0
zero_count=0
pos_count=0
neg_count=0
while(total_count<=10):
    num=int(input("Enter any integer ( 0 , negative or positive)"))
    number=int(num)
   
    
    if(number==0):
        zero_count+=1
    elif(number<=0):
        neg_count+=1
    else:
        pos_count+=1

    total_count+=1   
17.# Write a program to generate the fibonacci sequence upto n terms

n = int(input("Enter the number of terms for the Fibonacci sequence: "))

first_term = 0
second_term = 1

print("Fibonacci sequence:")

if n <= 0:
    print("Please enter a positive integer.")
elif n == 1:
    print(first_term)
else:
    print(first_term, second_term, end=' ')
    count = 2
    while count < n:
        next_term = first_term + second_term
        print(next_term, end=' ')
        first_term = second_term
        second_term = next_term
        count += 1
18.# write a program that reads a number and prints whether the number is a palindrome or not

number=int((input("Enter any number \n")))
if str(number)==str(number)[::-1]:
    print("The number is a palindrome")
else:
    print("The number is not a palindrome")
19.#write a program that finds all the armstrong number between 100 and 999
print("The list of armstrong numbers between 100 and 999 are:\n")
for number in range(101,999):
    num=str(number)
    first_digit=num[0]
    second_digit=num[1]
    third_digit=num[2]
    arm=int(first_digit)**3+int(second_digit)**3+int(third_digit)**3
    if(number==arm):
        print(number)

   20.  
Python program for menu based arithmetic operations
print("Simple Arithmetic Calculator")

print("\nSelect Operation:")
print("1. Addition (+)")
print("2. Subtraction (-)")
print("3. Multiplication (*)")
print("4. Division (/)")

choice = input("\nEnter your choice (1/2/3/4): ")


num1 = float(input("\nEnter the first number: "))
num2 = float(input("Enter the second number: "))


if choice == '1':
    result = num1 + num2
    print(f"\nResult: {num1} + {num2} = {result}")

elif choice == '2':
    result = num1 - num2
    print(f"\nResult: {num1} - {num2} = {result}")

elif choice == '3':
    result = n

       





