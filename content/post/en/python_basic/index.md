+++
date = '2026-03-17T15:24:19+09:00'
draft = true
title = 'Python_basic'
language = en
+++

### Section 1
print("Hellow world")
message = "Hellow world"  #source myenv/bin/activate
print(message)
name = "hellow world"
print(name.title())
print(name.upper())
print(name.lower())
first_name = "hellow"
last_name = "world"
fullname=first_name+"."+last_name
print(fullname)
real_name = " hellow world " 
print(real_name)
print(real_name.strip())#remove spaces
print(real_name.lstrip())#remove left space
print(real_name.rstrip())#remove right space
number=250
code = "The code is "+str(number)
print(code)
#Say hi to everyone!
print("Hellow world!".upper())
print("Hellow world!".lower()) 
print("Hellow world!".title())
varible = "Goodmorning"
old = varible #Store the previous value 
#cause the variable will be reassigned.
varible = "Goodevening" 
#Assign a new value to the existing variable.
print(varible + " world!")
### Section 2
import math # Give the access to python's built- in math module, which provides mathematical fuction and constans that aren't available by default.
result = math.sqrt(16)
print(result)
result = math.log2(8)
print(result)
import math
a = 1
b = 5
c = 3
delta = b**2 - 4*a*c
result1 = (-b+math.sqrt(delta))/(2*a)
result2 = (-b-math.sqrt(delta))/(2*a)
print(result1, result2)
### Section 3
Text1 = "Hellow world"
print(len(Text1)) # length of the string
print(Text1[2]) # indexing starts from 0, so Text1[2] will give us the 3rd character of the string, which is "l".
print(Text1[-1]) # negative indexing starts from the end of the string, so Text1[-1] will give us the last character of the string, which is "d".
print(Text1[0:5]) # slicing the string from index 0 to 4, which will give us "Hellow".
print(Text1[:5]) # slicing the string from the beginning to index 4, which will also give us "Hellow".
print(Text1[6:]) # slicing the string from index 6 to the end, which will give us "world".
a1=True    #Boolean value representing true
b1=False #Boolean value representing false
c1= None #None is a special value in Python that represents the absence of a value or a null value. It is often used to indicate that a variable has no value or that a function does not return anything.
print(type(a1)) # Output: <class 'bool'>
print(type(b1)) # Output: <class 'bool'>
print(type(c1)) # Output: <class 'NoneType'>
### Section 4
#BMI = weight (kg) / height^2 (m^2)
user_weight = float(input("Enter your weight in kilograms: "))
user_height = float(input("Enter your height in meters: "))
bmi = user_weight / (user_height ** 2)
print(f"Your BMI is: {bmi}") #f-string is a way to format strings in Python. It allows you to embed expressions inside string literals, using curly braces {}. The expressions are evaluated at runtime and their values are inserted into the string. In this case, {bmi} will be replaced with the value of the bmi variable when the string is printed.
#Or use print("Your BMI is: " + str(bmi)) #This will convert the bmi variable to a string and concatenate it with the rest of the message.
### Section 5
index1=int(input("Please enter your today's study time:"))
work_hard = int(input("Are you real working hard? (1 for yes, 0 for no): "))
if index1 >=3 and work_hard == 1:
    print("Great job! Keep up the good work!")
else:
    print("You need to work harder! Don't give up!")
# Different way to exposition
if index1 >=3:
    if work_hard == 1: # “==”: Comparison Operators
        print("Great job! Keep up the good work!")
    elif work_hard == 0:
        print("You need to work harder! Don't give up!")
if index1 < 3:
    print("You need to work harder! Don't give up!")
if work_hard != 1 and work_hard != 0: #“!=”: Not Equal To Operator
    print("Invalid input for work_hard. Please enter 1 for yes or 0 for no.")
### Section 6
mun_list=[1, 2, 3, 8, 0]
list_01=mun_list
print(list_01)
print(max(list_01))#max() function returns the largest item in an iterable or the largest of two or more arguments.
print(sorted(list_01)) #sorted() function returns a new sorted list from the items in an iterable. It does not modify the original list.
list_01.extend((5,9))#extend() method is used to add all the items of an iterable (like a list, tuple, or set) to the end of the list. In this case, it will add the numbers 5 and 9 to the end of the list_0.
list_01.remove(9) #remove() method is used to remove the first occurrence of a specified value from the list. In this case, it will remove the number 9 from the list_0.
print(list_01)
list_01.append((12,15,10,0.5,0.08)) #append() method is used to add a single item to the end of the list. In this case, it will add the tuple (12,15,10) to the end of the list_0.
print(list_01)

### Section 7
slang_dict = {"Jim":"123456",
             "Tom":"654321",
             "Lucy":"111111"} 
#A dictionary is a collection of key-value pairs, where each key is unique and maps to a specific value. In this case, the keys are tuples (e.g., ("Jim", 1)) and the values are strings (e.g., "123456"). The dictionary allows you to store and retrieve values based on their corresponding keys.
slang_dict["Wong"] = "222222" #This line adds a new key-value pair to the slang_dict dictionary. The key is the tuple ("Wong", 4) and the value is the string "222222". After this line is executed, the slang_dict will contain the new entry for Wong with the corresponding value.
del slang_dict["Tom"] #del statement is used to delete an item from a dictionary. In this case, it will remove the key-value pair with the key ("Tom", 2) from the slang_dict dictionary
print(slang_dict)
len(slang_dict) #len() function returns the number of items in a container. In this case, it will return the number of key-value pairs in the slang_dict dictionary, which is 4 after adding the new entry for Wong.
print(len(slang_dict))
name = input("Please enter the name: ")
if name in slang_dict:
    print(f"The number of {name} is: {slang_dict[name]}")
else:
    print(f"The {name} does not exist in the dictionary.")
temperature_dict ={"001":36.3,"002":37.2,"003":36.8,"004":38.5}
#A dictionary is a collection of key-value pairs, where each key is unique and maps to a specific value. In this case, the keys are strings (e.g., "001") and the values are floating-point numbers (e.g., 36.3). The dictionary allows you to store and retrieve values based on their corresponding keys.
print("The temperature of employee 002 is:", temperature_dict["002"]) #This line retrieves the value associated with the key "002" from the temperature_dict dictionary. In this case, it will return the value 37.2, which is the temperature corresponding to the key "002". The output will be 37.2
temperature_dict.keys()#keys() method is used to return a view object that displays a list of all the keys in the dictionary. In this case, it will return a view object containing the keys "001", "002", "003", and "004". The output will be dict_keys(['001', '002', '003', '004'])
print("The employee IDs are:",list(temperature_dict.keys())) 
temperature_dict.values() #values() method is used to return a view object that displays a list of all the values in the dictionary. In this case, it will return a view object containing the temperatures corresponding to the keys "001", "002", "003", and "004". The output will be dict_values([36.3, 37.2, 36.8, 38.5])
print(list(temperature_dict.values()))
temperature_dict.items() #items() method is used to return a view object that displays a list
print(list(temperature_dict.items())) 
for key, value in temperature_dict.items(): #items() method is used to return a view object that displays a list of key-value pairs in the dictionary. In this case, it will return a view object containing the key-value pairs ("001", 36.3), ("002", 37.2), ("003", 36.8), and ("004", 38.5). The for loop iterates through each key-value pair in the dictionary, allowing you to access both the key and the value in each iteration.
    if value >= 38:
        print(key+" has a fever!")
### Section 8
total = 0
for num in range(1, 101): #range() function is used to generate a sequence of numbers. In this case, it will generate numbers from 1 to 10 (inclusive). The for loop iterates through each number in the generated sequence, allowing you to perform operations on each number.
    total += num #This line adds the current number (num) to the total variable. The += operator is a shorthand for total = total + num, which updates the value of total by adding num to it. After the loop completes, total will contain the sum of all numbers from 1 to 10.
print(total)
list = ["1","2","3","4","5"]
for character in list:
    print(character)
#or
for i in range(len(list)): # len() return the number of items in the list; range(len()) generate the sequence.
    print(i,list[i])
list2 = ["1","2","3","4","5","6","7","8","9","10","11","12","13","14","15"]
i=0
while i < len(list2): # If the condition is true, the code block inside the while loop will be executed. 
    print(i,list2[i]) 
    i += 1 #i=i+1  #Every time the loop runs, it will increment the value of i by 1, which allows the loop to eventually terminate when i is no longer less than the length of list2.
### Section 9
total = 0
count = 0
user_input = input("Enter a number (or 'q' to quit): ")
while user_input!= "q" and count<10: # "！=" is the not equal to operator.
    num = float(user_input) # Change the user input from string to float.
    total += num # total = total + num
    count += 1 # count = count + 1
    user_input = input("Enter a number (or 'q' to quit): ") 
if count == 0: # "==" is the equal to operator.
        result = 0
else:
        result = total / count
print(f"The result is:{result:2f}") #f-string is the quote allows you to embed variables inside the string.
    #{} Inserts the value of the variable result into the string.
    #:2f formats the result to 2 decimal places.

Section 10
def calculate_bmi(weight, height):
    BMI = weight / (height ** 2)
    if BMI <= 18.5:
        category = "Underweight"
    elif BMI <= 25:
        category = "Normal weight"
    elif BMI <= 30:
        category = "Overweight"
    else:
        category = "Obesity"
    print(f"Your BMI is: {BMI:.2f}, which is categorized as {category}.") #f-string is a way to format strings in Python. It allows you to embed expressions inside string literals, using curly braces {}. The expressions are evaluated at runtime and their values are inserted into the string. In this case, {BMI:.2f} will be replaced with the value of the BMI variable formatted to 2 decimal places, and {category} will be replaced with the value of the category variable when the string is printed.
    return BMI, category #return statement is used to exit a function and return a value to
category_1 = calculate_bmi(70, 1.75) #This line calls the calculate_bmi function with the arguments 70 (weight in kilograms) and 1.75 (height in meters). The function will calculate the BMI based on the provided weight and height, determine the category of BMI, and print the result. The return statement in the function will return the calculated BMI and its category as a tuple, which will be stored in the variable category_1.
class cat:
    def __init__(self, name, age, color):
        self.name = name
        self.age = age
        self.color = color
    def speak(self):
        return self.words
cat1 = cat("A",6,"black") 
cat1.words = "Meow" 
cat2 = cat("B",5,"white")
cat2.words = "Purrr~"
print(f"{cat1.speak()}, my name is {cat1.name}, {cat1.age} years old, color is {cat1.color}") #This line attempts to print the name, age, and color attributes of the cat tuple. However, since cat is a tuple and not an object with attributes, this line will raise an AttributeError. To access the elements of the tuple, you should use indexing instead, like this: print(cat[0], cat[1], cat[2]) which will print the name, age, and color of the cat respectively.
print(f"{cat2.speak()}, my name is {cat2.name}, {cat2.age} years old, color is {cat2.color}")
class student:
    def __init__(self, name, student_id):
        self.name = name
        self.student_id = student_id
        self.grade = {"Math": 0, "English": 0, "Science": 0} 
    def set_grade(self, course, grade):
        if course in self.grade:
            self.grade[course] = grade
        else:
            print(f"Course {course} is not available.")
    def print_grands(self):
        print(f"Student Name: {self.name} (id: {self.student_id})'s grades are:")
        for course, grade in self.grade.items():
            print(f"{course}: {grade}")
Alice = student("Alice", "S001")
Alice.set_grade("Math", 85)
Alice.set_grade("English", 90)
Alice.set_grade("Science", 78)
Alice.print_grands()
Bob = student("Bob", "S002")
Bob.set_grade("Math", 92)
Bob.set_grade("English", 88)
Bob.set_grade("Science", 95)
Bob.print_grands()
print(Alice.name)
print(Bob.student_id)
print(Alice.grade)
### Section 11
class Employee:
    def __init__(self,name,id):
        self.name = name
        self.id = id
    def print_info(self):
        print(f"Name of the employee is {self.name}, and the id is {self.id}.")
class FulltimeEmployee(Employee):
    def __init__(self, name, id, month_salary):
        super().__init__(name, id) # super() function  inherits the name and id form the Employee class.
        self.month_salary = month_salary
    def calculate_monthly_pay(self):
        return self.month_salary   
class PartTimeEmployee(Employee):
   def __init__(self,name,id, daily_salary, work_days):
        super().__init__(name,id)
        self.daily_salary = daily_salary
        self.work_days = work_days
   def calculate_monthly_pay(self):
       return self .daily_salary * self.work_days
   
Wong = FulltimeEmployee("Wong", "001", 3000)
White = PartTimeEmployee("White", "002", 150, 20)
print(f"{Wong.name}'s monthly pay is: {Wong.calculate_monthly_pay()}")
print(f"{White.name}'s monthly pay is: {White.calculate_monthly_pay()}")

### Section 12
f = open("/home/jupiter/jiming/notes/programming/python/test.txt","r", encoding="utf-8") 
# "r" is only reading; "w" is only writing.
print(f.read())

f = open("/home/jupiter/jiming/notes/programming/python/test.txt","r", encoding="utf-8") 
line = f.readline()
while line != "":
    print(line)
    line = f.readline()
f = open("/home/jupiter/jiming/notes/programming/python/test.txt","r", encoding="utf-8") 
print(f.readlines())

f = open("/home/jupiter/jiming/notes/programming/python/test.txt","r", encoding="utf-8") 
lines = f.readlines()
for line in lines:
    print(line)
with open("/home/jupiter/jiming/notes/programming/python/test.txt") as f:
#with open("")as f:
    print(f.read())

### Section 13
with open("/home/jupiter/jiming/notes/programming/python/test2.txt","w", encoding="utf-8") as f:
    f.write("Four score and seven years ago our fathers brought forth on this continent,\n")
    f.write("a new nation, \n")
    f.write("conceived in Liberty, \n")
    f.write("and dedicated to the proposition that all men are created equal.\n")
with open("/home/jupiter/jiming/notes/programming/python/test2.txt","a", encoding="utf-8") as f:
   f.write("Now we are appending to the file.\n")
### Section 14
try:
    user_weight = float(input("Enter your weight in kilograms: "))
    user_height = float(input("Enter your height in meters: "))
    user_BMI = user_weight/user_height ** 2
except ValueError:
    print("Invalid input. Please enter numeric values for weight and height.")
except ZeroDivisionError:
    print("Height cannot be zero. Please enter a valid height.")
except:
    print("An unexpected error occurred. Please try again.")
else:
    print(f"Your BMI is: {user_BMI:.2f}")
finally:
    print("Thank you for using the BMI calculator.")