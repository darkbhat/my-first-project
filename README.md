
students = []

def add_student():
    name = input("Enter student name: ")
    roll = input("Enter roll number: ")
    course = input("Enter course: ")
    students.append({"name": name, "roll": roll, "course": course})
    print("Student added successfully!\n")

def view_students():
    if not students:
        print("No students found.\n")
        return
    print("\nStudent List:")
    for s in students:
        print(f"Name: {s['name']}, Roll: {s['roll']}, Course: {s['course']}")
    print()

def menu():
    while True:
        print("=== Student Management System ===")
        print("1. Add Student")
        print("2. View Students")
        print("3. Exit")
        choice = input("Enter your choice: ")

        if choice == "1":
            add_student()
        elif choice == "2":
            view_students()
        elif choice == "3":
            print("Exiting program...")
            break
        else:
            print("Invalid choice! Try again.\n")

menu()
