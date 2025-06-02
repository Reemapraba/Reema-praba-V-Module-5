# Reema-praba-V-Module-5
# 19CS301-Module5
### Register No - 212222020020
### Name - Reema praba V

# ExNo: 5.1 Python Constructors
### Aim: To Write a python code to create a student class with  default constructor  and a user defined function to display the text "welcome" with student name given to the function.
### Algorithm:

**STEP 1:** Start.

**STEP 2:** Define a class named `student`.

**STEP 3:** Inside the class, define a method `dis()`:
- Get user input and store it in the instance variable `self.a`.
- Print `"This is non parametrized constructor"`.
- Print a greeting message along with the input string.

**STEP 4:** Create an object `b` of class `student`.

**STEP 5:** Call the `dis()` method using object `b`.

**STEP 6:** Stop.

### Program:
```
class student:
    def dis(self):
        self.a = input()
        print("This is non parametrized constructor")
        print("Hello",self.a)
b = student()
b.dis()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/6b0d54a3-df82-413e-bf7e-dc8856d14768)

### Result: Thus, the given program is implemented and executed successfully .

# ExNo: 5.2 Python Destructors
### Aim: To Create  a  Python Class Student with a destructor.
### Algorithm:

**STEP 1:** Start.

**STEP 2:** Define a class named `Student`.

**STEP 3:** Inside the class, define a constructor method `__init__(self, name)`:
- Print `"Inside Constructor"`.
- Assign the parameter `name` to the instance variable `self.name`.
- Print `"Object initialized"`.

**STEP 4:** Define a method `say_hello(self)`:
- Print a greeting message using the instance variable `self.name`.

**STEP 5:** Define a destructor method `__del__(self)`:
- Print `"Inside destructor"`.
- Print `"Object destroyed"`.

**STEP 6:** Create an object `student` of the class `Student` and pass `"Emma"` as the argument.

**STEP 7:** Call the method `say_hello()` using the `student` object to display the greeting.

**STEP 8:** When the object goes out of scope or the program ends, the destructor is automatically invoked.

**STEP 9:** Stop.

### Program:
```
class Student:
    # Constructor method
    def __init__(self, name):
        print("Inside Constructor")
        self.name = name
        print("Object initialized")
    
    # Method to display student's name
    def say_hello(self):
        print(f"Hello, my name is {self.name}")
    
    # Destructor method
    def __del__(self):
        print("Inside destructor")
        print("Object destroyed")

# Creating an object of the Student class
student = Student("Emma")

# Calling the method to display the student's name
student.say_hello()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/6614e5d9-367e-471d-b5dc-4ff7f264af57)

### Result: Thus, the given program is implemented and executed successfully .

# ExNo: 5.3 Inheritance-1
### Aim: To Write a Python Program to Display the Employee Details EmpId , Emp Name., Gender,Company,DeptId.
### Algorithm:

**STEP 1:** Start.

**STEP 2:** Define a class named `details`.

**STEP 3:** Inside the class, define the constructor `__init__(self, a, b, c, d, e)`:
- Assign the parameters `a`, `b`, `c`, `d`, and `e` to instance variables `self.a`, `self.b`, `self.c`, `self.d`, and `self.e` respectively.

**STEP 4:** Define a method `disp(self)`:
- Print the employee details (ID, Name, Gender, Company, and DepartmentID) using the instance variables.

**STEP 5:** Get user input:
- Get an integer input for ID and store it in variable `a`.
- Get string input for Name, Gender, and Company, and store in variables `b`, `c`, and `d`.
- Get an integer input for DepartmentID and store in variable `e`.

**STEP 6:** Create an object `c` of class `details` using the collected inputs.

**STEP 7:** Call the `disp()` method using object `c` to display the employee details.

**STEP 8:** Stop.

### Program:
```
class details:
    def __init__(self,a,b,c,d,e):
        self.a =a
        self.b= b
        self.c= c
        self.d=d
        self.e=e
    def disp(self):
        print("Id\t\t:",self.a)
        print("Name\t\t:",self.b)
        print("Gender\t\t:",self.c)
        print("Company\t\t:",self.d)
        print("DepartmentID\t:",self.e)
a = int(input())
b = input()
c = input()
d = input()
e = int(input())
c = details(a,b,c,d,e)
c.disp()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/bf43641a-23c3-4395-be07-d4b3fdb288c4)

### Result: Thus, the given program is implemented and executed successfully .

# ExNo: 5.4 Inheritance-2
### Aim: To Write a Python program to Get the name, age and location of a person and display using Multilevel inheritance.
### Algorithm:

**STEP 1:** Start.

**STEP 2:** Define a base class named `getdetails`.

**STEP 3:** Inside the base class, define the constructor `__init__(self, a, b, c)`:
- Assign the parameters `a`, `b`, and `c` to the instance variables `self.a`, `self.b`, and `self.c`.

**STEP 4:** Define a derived class named `display` that inherits from `getdetails`.

**STEP 5:** Inside the `display` class, define a method `disp(self)`:
- Print the values of `self.a`, `self.b`, and `self.c` in a formatted way.

**STEP 6:** Get user input:
- Get a string input and store in variable `a`.
- Get an integer input and store in variable `b`.
- Get another string input and store in variable `c`.

**STEP 7:** Create an object `d` of the class `display` using the input values.

**STEP 8:** Call the `disp()` method using the object `d` to print the details.

**STEP 9:** Stop.

### Program:
```
class getdetails:
    def __init__(self,a,b,c):
        self.a =a
        self.b =b
        self.c =c
class display(getdetails):
    def disp(self):
        print(f"{self.a} {self.b} {self.c}")
a = input()
b = int(input())
c = input()
d = display(a,b,c)
d.disp()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/2ce25408-cc86-4000-858b-1ea033403fe7)

### Result: Thus, the given program is implemented and executed successfully .
 Exp.No:5(e)	HIERARCHICAL INHERITANCE

### AIM
To write a Python program to Get the employee  and doctor details & display it using Hierarchical inheritance.create a parent (base) class name Details and two child (derived) classes named Employee and Doctor
### ALGORITHM

Step 1:	  Begin the program.

Step 2:	 Create a class Details with an __init__ method to initialize three attributes: id, name, and gender.

Step a:	Define a method display_details() to print the values of id, name, and gender.

Step 3:	 Create a class Employee that inherits from the Details class.

Step a:	Add two additional attributes: company and department.

Step b:	Override the display_details() method to print the employee-specific attributes (company and department) along with the inherited details.

Step 4:	 Create a class Doctor that also inherits from the Details class.

Step a:	Add two additional attributes: hospital and department.

Step b:	Override the display_details() method to print the doctor-specific attributes (hospital and department) along with the inherited details.

Step 5:	 Accept input for employee and doctor details.

Step 6:	Create objects of Employee and Doctor using the input.

Step 7:	Call the display_details() method for both objects to print the details.Step 8:	

### PROGRAM
# Parent class Details
class Details:
    def __init__(self, id, name, gender):
        self.id = id
        self.name = name
        self.gender = gender

    def display_details(self):
        print(f"Id:  {self.id}")
        print(f"Name:  {self.name}")
        print(f"Gender:  {self.gender}")

# Child class Employee
class Employee(Details):
    def __init__(self, id, name, gender, company, department):
        # Call parent class constructor
        super().__init__(id, name, gender)
        self.company = company
        self.department = department

    def display_details(self):
        print("Employee Object")
        super().display_details()
        print(f"Company:  {self.company}")
        print(f"Department:  {self.department}")

# Child class Doctor
class Doctor(Details):
    def __init__(self, id, name, gender, hospital, department):
        # Call parent class constructor
        super().__init__(id, name, gender)
        self.hospital = hospital
        self.department = department

    def display_details(self):
        print("Doctor Object")
        super().display_details()
        print(f"Hospital:  {self.hospital}")
        print(f"Department:  {self.department}")

# Main function to get input and display details
def main():
    # Create Employee object and display details
    employee_id = int(input())
    employee_name = input()
    employee_gender = input()
    employee_company = input()
    employee_department = input()

    employee = Employee(employee_id, employee_name, employee_gender, employee_company, employee_department)
    employee.display_details()
    print("")
    # Create Doctor object and display details
    doctor_id = int(input())
    doctor_name = input()
    doctor_gender = input()
    doctor_hospital = input()
    doctor_department = input()

    doctor = Doctor(doctor_id, doctor_name, doctor_gender, doctor_hospital, doctor_department)
    doctor.display_details()

# Run the main function
main()

### OUTPUT
 ![image](https://github.com/user-attachments/assets/49f2eb5f-b9a6-4e0e-8b36-cae4cbe497e1)

### RESULT
Thus the python program for Hierarchical Inheritance to get the employee details was implemented and executed successfully.







