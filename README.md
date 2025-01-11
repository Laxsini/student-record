# student-record
import java.util.Scanner;


class Student {
    // Private fields (access modifiers used)
    private int rollNumber;
    private String name;
    private double marks;

    public Student(int rollNumber, String name, double marks) {
        this.rollNumber = rollNumber;
        this.name = name;
        this.marks = marks;
    }

    public int getRollNumber() {
        return rollNumber;
    }


    public void setRollNumber(int rollNumber) {
        this.rollNumber = rollNumber;
    }


    public String getName() {
        return name;
    }


    public void setName(String name) {
        this.name = name;
    }


    public double getMarks() {
        return marks;
    }


    public void setMarks(double marks) {
        this.marks = marks;
    }

    public void displayDetails() {
        System.out.println("Student Details:");
        System.out.println("Roll Number: " + rollNumber);
        System.out.println("Name: " + name);
        System.out.println("Marks: " + marks);
    }
}


public class StudentRecord {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        // Taking input for student details
        System.out.print("Enter Roll Number: ");
        int rollNumber = scanner.nextInt();


        scanner.nextLine(); // Consume newline left-over


        System.out.print("Enter Name: ");
        String name = scanner.nextLine();


        System.out.print("Enter Marks: ");
        double marks = scanner.nextDouble();
        Student student = new Student(rollNumber, name, marks);
        student.displayDetails();
        System.out.println("\nUpdating student details...");
        System.out.print("Enter new Name: ");
        scanner.nextLine(); // Consume newline
        String newName = scanner.nextLine();
        student.setName(newName);


        System.out.print("Enter new Marks: ");
        double newMarks = scanner.nextDouble();
        student.setMarks(newMarks);

        System.out.println("\nUpdated Student Details:");
        student.displayDetails();


        scanner.close();
    }
}


OUTPUT:
Enter Roll Number: 101
Enter Name: John Doe
Enter Marks: 85.5


Student Details:
Roll Number: 101
Name: John Doe
Marks: 85.5


Updating student details...
Enter new Name: Jane Smith
Enter new Marks: 92.3


Updated Student Details:
Roll Number: 101
Name: Jane Smith
Marks: 92.3

