# -Student-Grade-Manager
A beginner Python OOP project for managing student information, tracking grades, calculating averages, checking pass/fail status, and monitoring study hours. Built to practice Python classes, objects, methods, and lists.


    class Student:
         def __init__(self, name, age, grade):
         self.name = name
         self.age = age
         self.grade = grade
         
         def display_info(self):
              print(f"Name: {self.name} \nAge: {self.age}, \nGrade: {self.grade}")
         
         def grade_change(self, new_grade):
              self.grade = new_grade
              print(f"{self.name}'s new grade is {self.grade}")

         def pass_check(self):
              if self.avg_grade() >= 60:
                   return "Pass"
              else:
                   return "Fail"
         
         def studying(self, hours):
              print(f"{self.name} has been studying for {hours} hours")

         def add_grade(self, new_grade):
              self.grade.extend(new_grade)

         def avg_grade(self):
              return sum(self.grade) / len(self.grade)


    Arman = Student("Arman", 18, [90])
    Singh = Student("Singh", 22, [59])
    Alex = Student("Alex", 22, [60])

    Alex.add_grade([10, 10, 90, 50, 100])

    print(Alex.avg_grade())
    print(Alex.pass_check())
    print(Alex.display_info())
