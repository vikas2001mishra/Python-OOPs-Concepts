# Python-OOPs-Concepts


I.Object:- .Everything exist in this world i.e.object, object have behaviour and properties. 
           .Object is runtime entity.
  .For Example:- 
            obj = Dog()
II.Class:- .Class is a template.
          .class is a blueprint of an object.
          .class is the best example of encapsulation.
          .class is a user defined data type.


For Example Class & Object:-

# Object & Class Example-----

class Employee:
    '''This is a class which will calculate the salary of an employee'''
print(Employee.__doc__)
help(Employee)







# What is --init---
   # Constructor
   # --init--- is a constructor method,and automatically called to allocate memory, when a new object is created.


# What is Self() ---
  # self is used to represent the instance(object) of the class.
  
  # self is a Python Provided implict default variable which is always pointing to current object.
  # By using self we can access variables, metheds of corresponding objet.
  # In Constructor self should be the Frist arg (argument).
  # Self is the 1st argument in the instance method as well.





  # Types of variable in Python:
     1.Instance (Object level variable)
     2.Static (Class level variable)
     3.Local (Method level variable)
     
# 1.Instance variable:-
                       For every object a seperate copy will be created.
# 2.Static variable:-
                       Only one copy will be created at the class level.
                       

# Types of methods:-
         1. Instance methods (Object related method)
         2. Static methods
         3. class method

   

# Instance methods:-
            -> Object related method.
            -> Any method consists of Instance variable-Instance method,
            -> Inside the instance method, First Keyword, i.e. self is compulsory.


# Setter and getter methods:-
      .Setter-> To set the value to the Instance variale (mutator method)->(other name Setter).
      .getter-> To get the value to the Instance variable.,also knoen as (Accessor method).


# Static methods:-
            ->Inside methed if we are not using instance and static variables.
            ->General utility method
            ->@staticmethed

# class method:-
            ->Inside the methed Implementation of we are using only static variable (without Instance variables).
            ->Atleast one Instance variable - instance method.
            ->Instance method + Static variable -> Both are present (Instance method).
           
            @classmethod # Decorator
            cls
            we can call class method by using class or object ref.


# Note:-
     ->Instance methed - (No decorator required)
     ->class method - @classmethed is (mandatory)
     ->static method - @staticmethed is (optional)

# Note:- 
     ->Instance variables - (Instance method)
     ->static variable - (class method)
     ->Instance + Static- (Instance method)
     ->Instance + local- (Instance method)
     ->static + local (Class method)
     ->local (static method)

# No decorator:-  only two options.
     ->Instance method
     ->Static metheed
     

     
                   


   
# 1.First Program:-

class Employee:
    def __init__(self,fname,lname,salary):
        self.fname = fname
        self.lname = lname
        self.salary = salary

vikas = Employee('vikas','mishra',50000)
Rohan = Employee('Rohan','kumar',40000)
print(Rohan.salary,vikas.salary)




# Other Method:-

class Employee:
    def __init__(self,fname,lname,salary):
        self.fname = fname
        self.lname = lname
        self.salary = salary
    def info(self):
        print(self.fname)
        print(self.lname)
        print(self.salary)
emp = Employee("Rahul","Sharma",1000)
emp.info()




# 2. Employee Salary Increment?

class Employee:
    increment = 2.5
    def __init__(self,fname,lname,salary):
     self.fname = fname
     self.lname = lname
     self.salary = salary
    def increase(self):
        self.salary = self.salary * Employee.increment
mukesh = Employee("mukesh","mishra",5000)
mukesh.increase()
print(mukesh.salary)




# 3. celsius to fahrenheit?

def ctof(c):
    f = (c*9/5)+32
    print(f)
ctof(10)
ctof(20)
ctof(30)


# Other Method:


class Ctof:
    def __init__(self,c):
        self.c = c
    def ctof(self):
        f = (self.c*9/5) + 32
        print(f)
c1 = Ctof(10)   
c2 = Ctof(20)      #object
c3 = Ctof(30)
c4 = Ctof(40)
c1.ctof()
c2.ctof()
c3.ctof()
c4.ctof()





# 4. Employee,name,employeeid,salary:-


class Employee:
    def __init__(self,name,employeeid,salary):
        self.name = name
        self.employeeid = employeeid                 # These three are instance variables.
        self.salary = salary
    def talk(self):       #its not a function ,talk is a method
        print("hello my name is:",self.name)
        print("hello my employeeid is:",self.employeeid)
        print("hello my salary is:",self.salary)
emp1 = Employee("Suresh",1234,56789)
emp2 = Employee("Ramesh",1290,56700)
emp1.talk()
emp2.talk()





# 5.Movie Example:

class Movie:
    def __init__(self,name,hero,heroine,rating):
        self.name = name
        self.hero = hero
        self.heroine = heroine
        self.rating = rating
    def info(self):
        print("movie name:",self.name)
        print("movie hero:",self.hero)
        print("movie heroine:",self.heroine)
        print("movie rating:",self.rating)
mov = Movie("PK","AK","AS",10)
mov.info()





# 6.Movie Example through for loop:-


class Movie:
    def __init__(self,name,hero,heroine,rating):
        self.name = name
        self.hero = hero
        self.heroine = heroine
        self.rating = rating
    def info(self):   #info is method
        print("movie name:",self.name)
        print("movie hero:",self.hero)
        print("movie heroine:",self.heroine)
        print("movie rating:",self.rating)
movies = [Movie("PK","AK","AS",10),Movie("AB","CD","EF",10),Movie("GH","IJ","KL" ,6),Movie("MN","OP","QR",0 )]
for mov in movies:
    mov.info()






# How to access the instance variable.
   # Within the class by using self.

# 7.

class Test:
    def __init__(self):
        self.a = 20
        self.b = 30
    def m1(self):
        print(self.a)
        print(self.b)
t = Test()
t.m1()
#print(t.a)
#print(t.b)






# 8. write Fibonacci series up to n

def fib(n):   
     #""""Print a Fibonacci series up to n.""""
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a+b
    

# Now call the function we just defined:
fib(2000)




# 9.return Fibonacci series up to n

def fib2(n):  
    """Return a list containing the Fibonacci series up to n."""
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)    # see below
        a, b = b, a+b
    return result

f100 = fib2(100)    # call it
print(f100)







# 10.Static Variables......

class Test:
    a = 10 #static variable
    def __init__(self):
        Test.b = 20
    def m1(self):
        Test.c = 30
    @classmethod
    def m2(cls):
        cls.d = 40
        Test.e = 50
    @staticmethod
    def m3():
        Test.f = 60
#print(Test.___dict__)
t = Test()
#print(Test.__dict__)
t.m1()
#print(Test.__dict__)
t.m2()
#print(Test.__dict__)
t.m2()
print(Test.__dict__)







# 11. Instance variable & Static Variable

class Test:
    a = 777
    def __init__(self):
        self.a = 888
t = Test()
print(t.a) #Instance variable
print(Test.a) #Static Variable








# 12.How to access the Static Variable...

class Test:
    a = 10
    def __init__(self):
        print(self.a)           #constuctor method
        print(Test.a)

    def m1(self):
        print(self.a)           #Instance method
        print(Test.a)

    @classmethod
    def m2(cls):
        print(cls.a)           #class method
        print(Test.a)

    @staticmethod
    def m3():                  #Static method
        print(Test.a)
t = Test()
t.m1()
t.m2()
t.m3()








# 13.Where we can modify the value of Static variables:

class Test:
    a = 10
    def __init__(self):
        Test.a = 100           #update value
t = Test()
print(Test.a)





# 14.

class Test:
    a = 10
    def __init__(self):
        Test.a = 888
    def m1(self):
        Test.a = 999
t = Test()
print(Test.a)
t.m1()
print(Test.a)








# 15.Local Variable...

class Test:
    def m1(self):
        a = 100
        print(a)
    def m2(self):
        b = 200
        print(b)
t = Test()
t.m1()
t.m2()









# 16. Instance Method---

class Student:
    def __init__(self,name,marks):
        self.name = name
        self.marks = marks
    def display(self):
        print('hi',self.name)
        print('your marks are:',self.marks)
    def grade(self):
        if self.marks>=60:
            print("you got 1st div.")
        elif self.marks>=50:
            print("yor got 2nd div.")
        elif self.marks>=33:
            print("you got 3rd div.")
        else:
            print("you did not pass")
s = Student("Rahul",69)
s.display()
s.grade()












# 17.Setter and Getter Concept ............ ReCheck
class Student:
    def setName(self,name):
        self.name = name
    def getName(self):
        return self.name
    def setMarks(self,marks):
        self.marks = marks
    def getMarks(self):
        return self.marks
l = []
n = int(input("Enter the name of the  student"))
for i in range(n):
    s = Student()
    name = input("Enter the student name")
    marks = int(input("Enter marks"))
    s.setName(name)
    s.setMarks(marks)
    l.append(s)
for s in l:
    print("Student Name",s.getName())
    print("Student Marks",s.getMarks())
    print()












# 18.Class Method:-

class Employee:
    total_emp = 10
    @classmethod
    def totemp(cls,compname):
        print("{} has total {} employees".format(compname,cls.total_emp))
Employee.totemp('TCS')


# 19.

class Test:
    count = 0
    def __init__(self):
        Test.count = Test.count+1
    @classmethod
    def noofobj(cls):
        print("The no of object created",Test.count)
t1 = Test()
t2 = Test()
t3 = Test()
Test.noofobj()










# 20.static method:-

class Rahulmarks:
    @staticmethod
    def add(x,y):
        print('the sum is:',x+y)
    @staticmethod
    def product(x,y):
        print('the product is:',x*y)
    @staticmethod
    def average(x,y):
        print('the avg is:',(x+y)/2)
Rahulmarks.add(10,20)
Rahulmarks.product(10,20)
Rahulmarks.average(10,20)









# 21. Passing The members of one class to another ......?

class Employee:
    def __init__(self,eno,ename,esal):
        self.eno = eno
        self.ename = ename
        self.esal = esal

    def display(self):
        print("Emoloyee No:",self.eno)
        print("Emoloyee Name:",self.ename)
        print("Employee Sal:",self.esal)

class Test:
    def Modify(emp):
        emp.esal = emp.esal+10000
        emp.display()

e = Employee(100,"Rahul",15000)
#e.display()
Test.Modify(e)



# 22.

class Test:
    def Modify(emp):
        print('Hello')
e = Test()
e.Modify() #Instance
Test.Modify(56) #Static Method










# 23. Ineer Classes
    # Classes Inside the another classes.
    # Without exixting outer class inner class is of no use.



class Outer:
    def __init__(self):
        print("outer class object creation...")

    class Inner:
        def __init__(self):
            print("Inner class object creation...")

        def m1(self):
            print("Ineer Class Method")

#i = Outer().Inner().m1()
o = Outer()
i = o.Inner()
i.m1()



# 24.

class Outer:
    def __init__(self):
        print("outer class object creation...")
    class Inner:
        def __init__(self):
            print("Inner class object creation...")
        class InnerInner:
            def __init__(self):
                print("Inner Inner clas object creation...")
            def m1(self):
                print("Inner Inner class Method")
i =Outer().Inner().InnerInner().m1()


# 25.

class Human:
    def __init__(self):
        self.name = 'Rahul'
    def display(self):
        print("Hello",self.name)
h=Human()
h.display()


# 26.

class Human:
    def __init__(self):
        self.name = 'Rahul'
        self.head = self.Head()
        self.brain = self.head.Brain()

    def display(self):
        print("Hello",self.name)
        self.head.talk()
        self.brain.think()

    class Head:
        def talk(self):
            print("Talking.....")
        class Brain:
            def think(self):
                print("Thinking...")
h=Human()
h.display()
h.Head()









# 27.Garbage Collector...
      ->GC is the part OF Python virtual machine.
      ->GC is the process of removing any object which are not being used by any other object.


import gc
print(gc.isenabled())
gc.disable()
print(gc.isenabled())
gc.enable()
print(gc.isenabled())











# III. INHERITANCE:-
      # Inheritance used code reusability.
      # Inheritance is a relationship between two or more classes.
      # Inheritance is a real world relationship.

  . Inheritance concept into two categories:-
        # Subclass(child class)
        # Superclass(Parent class)


# 1.

class Car:
    def __init__(self,name,model,color):
        self.name = name
        self.model = model
        self.color = color

    def getinfo(self):
        print("Car Name:",self.name)
        print("Car Model:",self.model)
        print("car color:",self.color)
    def getinfo(self):
        print("Car Model:" + self.name)
c=Car("Maruti 800",800,"White")
c.getinfo()



# 2. 

class Car:
    def __init__(self,name,model,color):
        self.name = name
        self.model = model
        self.color = color

    def getinfo(self):
        print("Car Name:",self.name)
        print("Car Model:",self.model)
        print("car color:",self.color)

class Employee:
    def __init__(self,eno,ename,car):
        self.eno = eno
        self.ename = ename
        self.car = car

    def empinfo(self):
        print("Employee NO:",self.eno)
        print("Employee Name:",self.ename)
        print("car information--->")
        self.car.getinfo()

c=Car("Maruti 800",800,"White")
e = Employee(100,"Satish",c)
e.empinfo()





# TYPES OF INHERITANCE:-
-> TRICk- SMM HH

1.Single Inheritance.
2.Multilevel Inheritance.
3.Multiple Inheritance.
4.Hierarchical Inheritance.
5.Hybrid Inheritance.


# 1.Single Inheritance.->
                      Single parent, single child. 

# For Example->

# 3.

class P:
    def  m1(self):
        print("Parent method")
class C(P):
    def m2(self):
        print("Child method")
c=C()
c.m1()
c.m2()






# 2.Multilevel Inheritance:->
     -> In multilevel inheritance, features of the base class and the derived class are further inherited into the new derived class. 
     This is similar to a relationship representing a child and a grandfather. 

# 4.

class P:
    def m1(self):
        print("Parent method")
class C(P):
    def m2(self):
        print("Child method")
class CC(C):
    def m3(self):
        print("Sub-child method")
cc=CC()
cc.m1()
cc.m2()
cc.m3()



# 3.Multiple Inheritance:->
       -> When a class is derived from more than one base class it is called multiple Inheritance. 


# 5.

class P1:
    def m1(self):
        print("Parent 1 method")
class P2:
    def m2(self):
        print("Parent 2 method")
class C(P1,P2):
    def m3(self):
        print("child method")
c = C()
c.m1()
c.m2()
c.m3()




# 4.Hierarchical Inheritance.
      -> Hierarchical Inheritance If multiple derived classes are created from the same base, 
      this kind of Inheritance is known as hierarchical inheritance. 


# 6.

class P:
    def m1(self):
        print("Parent class")
class C1(P):
    def m2(self):
        print("Child 1 method")
class C2(P):
    def m3(self):
        print("Child 2 method")

c = C1()
c.m1()
c.m2()
#c1.m3()
c = C2()
c.m3()


# 5.Hybrid Inheritance-> 
           -> Hybrid Inheritance is a combination of multiple Inheritance and multilevel inheritance.


# 7.

class A:
    def m1(self):
        print("Class A method")
class B(A):
    def m2(self):
        print("Class B method")
class C(A):
    def m3(self):
        print("Class C method")
class D(B,C):
    def m4(self):
        print("Class D method")

d = D()
d.m1()
d.m2()
d.m3()
d.m4()







# Super()->
      which can be used to call parent class. Constructor, methods and variables from the child class.


# 8.

class Person:
    def __init__(self,name,age):
        self.name = name
        self.age = age
class Student(Person):
    def __init__(self,name,age,rollno,marks):
        self.name = name
        self.age = age
        self.rollno = rollno
        self.marks = marks
    def display(self):
        print(self.name)
        print(self.age)
        print(self.rollno)
        print(self.marks)
s = Student("Rahul",22,46,87)
s.display()


# 9.

class Person:
    def __init__(self,name,age):
        self.name = name
        self.age = age
    def display1(self):
        print(self.name)
        print(self.age)


class Student(Person):
    def __init__(self,name,age,rollno,marks):
        super().__init__(name,age)
        self.rollno = rollno
        self.marks = marks

    def display2(self):
        super().display1()
        print(self.rollno)
        print(self.marks)
s = Student("Rahul",22,46,87)
s.display2()
s.display1()



      




















          
