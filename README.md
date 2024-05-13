Problem Formulation: Student enrollment 

Inputs:

Student ID (for adding and removing a student): A unique identifier for each student.
Name: Name of the student.
Grade Level: The level or year of schooling for the student.
Courses (for adding a student): List of courses the student is enrolled in. 

outputs: 
Success or failure messages for adding or removing students.
List of enrolled students with their details (ID, name, grade level, and enrolled courses)

Parts of the Problem:

Add a New Student:
Inputs: Student ID, name, grade level, courses.
- Check if the student ID is already in the system.
Output: You would get a messge saying the student is added successfully. if not administrator will recieve a failure

Remove a Student:
Input: Student ID.
Check if the student ID exists in the system, if yes, remove the student from the system.
Output: Success message if the student is removed successfully, otherwise, a message indicating failure

View Enrolled Students:
- Display the details of all enrolled students.
Output: List of enrolled students with their student information

class StudentEnrollmentSystem:
    def instructor (self):
        self.students = {}
        
    def add_student(self, student_id, name, grade_level, courses):
        if student_id in self.students:
            print("Student ID already exists. Please choose a different ID.")
            return False
        self.students[student_id] = {'name': name, 'grade_level': grade_level, 'courses': courses}
        print("Student added successfully.")
        return True
