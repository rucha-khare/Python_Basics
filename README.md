# Python_Basics
Below are the problems that I solved while learning the basics of Python.



#1 In a certain encrypted message which has information about the location(area, city), the characters are jumbled such that first character of the first word is followed by the first character of the second word, then it is followed by second character of the first word and so on.

string = input()
message1 = string[::2]
message2 = string[1::2]
print(message1+','+message2)



#2 Remove SPSS from input_list=['SAS', 'R', 'PYTHON', 'SPSS'] and add 'SPARK' in its place.

import ast,sys
input_list = (sys.stdin.read()).split(',')
input_list[3]='SPARK'
print(input_list)




#3 Convert a list ['Pythons syntax is easy to learn', 'Pythons syntax is very clear'] to a string using ‘&’.

import ast,sys
input_str = (sys.stdin.read()).split(',')
input_str[1]= "&"
input_str.extend(['Pythons syntax is very clear'])
input_str
string_1 = (' '.join(input_str))
print (string_1)




#4 Split the string input_str = 'Kumar_Ravi_003' to the person's second name, first name and unique customer code. In this example, second_name= 'Kumar', first_name= 'Ravi', customer_code = '003'.

import ast,sys
input_str = sys.stdin.read()
first_name = input_str.split('_')[1]
second_name = input_str.split('_')[0]
customer_code = input_str.split('_')[2]
print(first_name)
print(second_name)
print(customer_code)




#5 Add the element ‘Python’ to a tuple input_tuple = ('Monty Python', 'British', 1969). Since tuples are immutable, one way to do this is to convert the tuple to a list, add the element, and convert it back to a tuple.

import ast,sys
input_str = sys.stdin.read()
input_tuple = ast.literal_eval(input_str)
x = list(input_tuple)
y = x + ["Python"]
tuple_2 = tuple (y)
print(tuple_2)




#6 Let’s say you have two lists A and B. Identify the elements which are common in the two lists A and B and return them in a sorted manner
import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
list_1 = input_list[0]
list_2 = input_list[1]
C = set (list_1)
D = set (list_2)
I = (C&D)
print(sorted(I))




#7 Write code to fetch the profession of the employee with Employee id - 104 from an employee input given in the form of a dictionary where key represent employ id and values represent the name, age, and profession (in the same order).

import ast,sys
input_str = sys.stdin.read()
input_dict = ast.literal_eval(input_str)
profession = (input_dict[104][2])
print(profession)




#8 From a Dictionary input_dict={'Name': 'Monty', 'Profession': 'Singer' }, get the value of a key ‘Label’ which is not a part of the dictionary, in such a way that Python doesn't hit an error. If the key does not exist in the dictionary, Python should return 'NA'.

import ast,sys
input_str = sys.stdin.read()
input_dict = ast.literal_eval(input_str)
answer = input_dict.get("Label", "NA")
print(answer)




#9 Create a SORTED list of all values from the dictionary input_dict = {'Jack Dorsey' : 'Twitter' , 'Tim Cook' : 'Apple','Jeff Bezos' : 'Amazon' ,'Mukesh Ambani' : 'RJIO'}

import ast,sys
input_str = sys.stdin.read()
input_dict = ast.literal_eval(input_str)
print (sorted(input_dict.values()))




#10 Write a code to check if the string in input_str starts with a vowel or not. Print capital YES or NO.

import ast,sys
input_str = sys.stdin.read()
if input_str[0]=="a" or input_str[0]=="e" or input_str[0]=="i" or input_str[0]=="o" or input_str[0]=="u":
    print ("YES")
else:
    print ("NO")




#11 You are given a list of string elements and asked to return a list which contains each element of the string in title case or in other words first character of the string would be in upper case and remaining all characters in lower case

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
new_list = []
for val in input_list:
    new_list.append(val.title())
print (new_list)




#12 You are given an integer 'n' as the input. Create a list comprehension containing the squares of the integers from 1 till n^2 (including 1 and n), and print the list. 

import ast, sys
n = int (input ())
l1 = [i**2 for i in range (1,n+1)]
print (l1)




#13 Extract the words that start with a vowel from a list input_list=[wood, old, apple, big, item, euphoria] using list comprehensions.

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
list_vowel =[word for word in input_list if word[0] in "aeiou"]
print(list_vowel)




#14 Create a function squared(), which takes x and y as arguments and returns the x**y value. For e.g., if x = 2 and y = 3 , then the output is 8.

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
x = int(input_list[0])
y = int(input_list[1])
def squared(x,y):
    return x**y
print(squared(x,y))




#15 Create a lambda function 'greater', which takes two arguments x and y and return x if x>y otherwise y.
If x = 2 and y= 3, then the output should be 3.

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
a = int(input_list[0])
b = int(input_list[1])
f = lambda a,b: a if a>b else b
print (f(a,b))




#16 Using the function Map, count the number of words that start with ‘S’ in input_list.

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
f = lambda x: x[0] == 'S'
count= list (map(f, input_list)).count(True)
print (count)




#17 Create a list ‘name’ consisting of the combination of the first name and the second name from list 1 and 2 respectively. 

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
first_name = input_list[0]
last_name = input_list[1]
name = map(lambda x,y : x+' '+y, first_name,last_name)
print(list(name))




#18 Extract a list of numbers that are multiples of 5 from a list of integers named input_list.

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
divby5 = lambda x : x%5 == 0
list_answer = list (filter (divby5, input_list))
print (list_answer)




#19 You are given a list of strings such as input_list = ['hdjk', 'salsap', 'sherpa'].
Extract a list of names that start with an ‘s’ and end with a ‘p’ (both 's' and 'p' are lowercase) in input_list.

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
sp = list (filter(lambda x: x.startswith ('s') and x.endswith ('p'), input_list))
print(sp)




#20 Using the Reduce function, concatenate a list of words in input_list, and print the output as a string.
If input_list = ['I','Love','Python'], the output should be the string 'I Love Python'.

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
import functools
answer = (functools.reduce(lambda x,y : x+ " " +y, input_list))
print (answer)




#21 You are given a list of numbers such as input_list = [31, 63, 76, 89]. Find and print the largest number in input_list using the reduce() function.

import ast,sys
input_str = sys.stdin.read()
input_list = ast.literal_eval(input_str)
import functools
answer = (functools.reduce(lambda a,b : a if a > b else b, input_list)) 
print(answer)




#22 You are given two integer variables,  x and y. You have to swap the values stored in x and y.

in_string=input()
list1= in_string.split(",")
x=list1[0]
y=list1[1]
print ('x before swapping:{0}'.format(x))
print ('y before swapping: {0}'.format(y))
z=x
x=y
y=z
print ('x after swapping: {0}'.format(x))
print ('y after swapping:{0}'.format(y))




#23 A number k is beautiful if it is of the form 3n+1, is pretty if it is of the form 3n+2 and is sexy if it is of form 3n.
Given a number k, print if it is beautiful, pretty or sexy.

k=int(input())
if k%3 == 0:
    print ('sexy')
elif k%3 == 1:
    print ('beautiful')
elif k%3 == 2:
    print ('pretty')
   
   
   
   
#24 Compute and display Fibonacci series upto n terms where n is a positive integer entered by the user.

n= int(input())
n1 = 0
n2 = 1
if n<= 0:
    print ("0")
else: 
    print (n1)
    print (n2)
    for i in range (2,n):
        next= n1+n2
        print (next)
        n1=n2
        n2=next
   
   
   
   
#25 Write python code to find the sum of prime numbers from 2 to n where n is a positive integer entered by the user.

n = int(input())
pn= []
for i in range (2,n+1):
    for j in range (2,i):
        if (i%j) == 0:
            break
    else:
        pn.append(i)
print (sum(pn))



#26 Earlier you solved the chocolate problem where Sanjay had m rupees and cost of each chocolate was c rupees. Shopkeeper gave away one chocolate for three wrappers. In this problem lets generalise the question saying, Sanjay has m rupees, each chocolate costs c rupees, shopkeeper will give away k chocolates for w wrappers. Can you find now how many chocolates Sanjay will be able to eat?

input_string= input()
list1= input_string.split(",")
m= int(list1[0])
c= int(list1[1])
w= int(list1[2])
k= int(list1[3])
choc= m//c
wrap= m//c
while wrap//w != 0:
    choc= choc + ((wrap//w)*k)
    wrap= ((wrap//w)*k) + (wrap%w)
print (choc)



#27 Description
You are given a row of Lego Blocks consisting of n blocks. All the blocks given have a square base whose side length is known. You need to stack the blocks over each other and create a vertical tower. Block-1 can go over Block-2 only if sideLength(Block-2)=>sideLength(Block-1).
From the row of Lego blocks, you can only pick up either the leftmost or rightmost block.
Print "Possible" if it is possible to stack all n cubes this way or else print "Impossible".

import ast
sides= ast.literal_eval(input())
tower= []
while sides:
    if sides[0]>=sides[-1]:
        tower.append(sides.pop(0))
    else:
        tower.append(sides.pop())
for i in range (len(tower)-1):
    if tower[i]<tower[i+1]:
        print ('Impossible')
        break
else:
    print ('Possible')
   
   
    
#28 Write a Python program to divide a given list to chunks of size k.
The number of elements in the list need not to be divisible by k.
For example, if you want to divide the list [1,2,3,4,5,6,7] into chunk size k=4, then the first chunk will be [1,2,3,4] and the second one will have [5,6,7]. i.e. the last chunk need not have k elements. The input will have two lines, the first line would have the list and the second line would have the value of k.
The final output should have the list chunks in different lines.

import ast
input_str = input()
input_list = ast.literal_eval(input_str)
l=input_list[0]
k=input_list[1]
for i in range(0,len(l),k):
    print (l[i:i+k])
 
 
  
#29 Given a list of numbers, find the second largest number in the list.

import ast
l = ast.literal_eval(input())
r = [] 
for i in l: 
    if i not in r: 
        r.append(i)
if len(r) == 1:
    print('not present')
else:
    r.sort(reverse= True)
    print (r[1])
    
    
    
#30 Given two strings, one of the strings will contain an extra character. Find the extra character. The number of all the other characters in both the strings will be the same. Check the sample input/output for more clarification.
The code will be case sensitive.

s1= input()
s2= input()
s1= s1.lower()
s2= s2.lower()
for i in s2:
    if i not in s1:
        print (i)
      
      
        
#31 You will be given a string as input. You just have to determine if the string can be an integer or no?

n= input()
n= n.strip()
s= 0
num= '0123456789'
for i in n[1:]:
    if i not in num:
        s=1
if n[0] not in num + '-':
    s=1
if s>0:
    print('STR')
else:
    print ('INT')
    
    
    
#32 While extracting data from different sources, often numeric values come in string format and with commas like 1,000 or 23,321 and also sometimes with spaces in start and beginning of the string. For simplicity, we will consider only integer values imbedded with commas. You will take the input and print the cleaned integer without commas and spaces.

n= input()
n= n.replace(",", "")
n1= n.split()
n2= "".join(n1)
print (n2)



#33 You write all your passwords in a diary so that you don't forget them. But clearly this is too risky, so you came up with a simple plan, you will simply write it by shifting all the alphabets by a certain step. For eg: if you decide your step to be 3, then 'a' will become 'd', and 'k' will become 'n' and so for all alphabets. The last alphabets will simply circle back to 'a'. In this case, 'y' will become 'b' and so on. Now you just have to remember the step size, can then you can check the password anytime you want. You decided to write code to do this, now that you have learned coding in python. Your code will take in the step size and what is written in the diary and give out the real password.

import ast
I= ast.literal_eval(input())
w= I[0]
s= int(I[1])
L= 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
l= L.lower()
new = ''
for i in w:
    if i in L:
        new= new+ L[L.index(i)-s]
    else:
        new= new+ l[l.index(i)-s]
print (new)



#34 Write a program that computes the value of n+nn+nnn+nnnn+... nn...n ntimes with a given number as the value of n.

n= int(input())
m=''
t= 0
for i in range (0,n):
    m=''
    for j in range (0,i+1):
        m= m+str(n)
    t= t+ int(m)
print (t)



#35 You will be given a dictionary with keys as items and values as their prices. You have to print the cheapest item. 

import ast
d= ast.literal_eval(input())
v=  min(d.values())
for k in d:
    if d[k]== v:
        v=k
        print('{0}: {1}'.format(v,d[v]))
    
    

#36 You will be given a list of repeated elements. You have to find the maximum distance between two same elements. The answer will be zero if there are no repeated elements.

import ast
l= ast.literal_eval(input())
md= 0
for i in range(len(l)-1):
    d=0
    for j in range(i+1,len(l)):
        if l[i]==l[j]:
            d=j-i
    if (md<d):
        md=d
print(md)



#37 Your team is going for camping and you are taking a vote to decide what food to pack for dinner.
Everyone gets a vote and the food item that gets at least one more than half of the votes wins. None of the items wins if nothing gets at least one more than half votes. Assume that every person gets only one vote.
The input will contain a list of food items where each occurrence of an item represents one vote. You should print the winning food item as output. If there is no clear winner, print "NOTA". 

import ast
votes = ast.literal_eval(input())
v= len(votes)
d= {}
for i in votes:
    if i not in d:
        d[i]=1
    else:
        d[i]= d[i]+1
winner=False
for j in d:
    if d[j]>v//2:
        print(j)
        winner=True
        break
if not winner:
    print ('NOTA')
    


