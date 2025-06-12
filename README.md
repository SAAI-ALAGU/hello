import java.util.Scanner;

class Student {
    private String name;
    private String rollNumber;
    private String department;

    public Student(String name, String rollNumber, String department) {
        this.name = name;
        this.rollNumber = rollNumber;
        this.department = department;
    }

    public void printIDCard() {
        System.out.println("==================================");
        System.out.println("         V.S.B ENGINEERING COLLEGE");
        System.out.println("==================================");
        System.out.println("Name       : " + name);
        System.out.println("Roll No.   : " + rollNumber);
        System.out.println("Department : " + department);
        System.out.println("==================================");
    }
}

public class IDCardGenerator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter Student Name:");
        String name = scanner.nextLine();

        System.out.println("Enter Roll Number:");
        String rollNumber = scanner.nextLine();

        System.out.println("Enter Department:");
        String department = scanner.nextLine();

        Student student = new Student(name, rollNumber, department);

        System.out.println("\nGenerating ID Card...\n");
        student.printIDCard();

        scanner.close();
    }
}
