students = {}

def add_student(name, subject, grade):
    students[name] = (subject, grade)

def view_students():
    print("Student Records:")
    for name, data in students.items():
        subject, grade = data
        print(f"{name} -> {subject}: {grade}")
while True:
    name = input("Enter student name:")
        
    subject = input("Enter subject: ")
    grade = int(input("Enter grade: "))
    add_student(name, subject, grade)
    
    more = input("do you want to add another student? (yes,no): ")
    if more.lower() != "yes":
        break
view_students()
