import java.util.Scanner;
public class GradeApp {
public static void main(String[] args){


   Scanner scanner = new Scanner(System.in);


   // Student name
   System.out.println("Enter Student Name: ");
   String name = scanner.nextLine();


   // Student ID
   System.out.println("Enter Student ID: ");
   int id = scanner.nextInt();
   scanner.nextLine();


   // Course 1
   System.out.println("Enter Course 1: ");
   String course1 = scanner.nextLine();
   System.out.println("Enter credit hours for Course 1: ");
   int credit1 = scanner.nextInt();
   System.out.println("Enter Course 1 Grade:");
   double course1Grade = scanner.nextDouble();
   scanner.nextLine();


   // Course 2
   System.out.println("Enter Course 2:");
   String course2 = scanner.nextLine();
   System.out.println("Enter credit hours for Course 2: ");
   int credit2 = scanner.nextInt();
   System.out.println("Enter Course 2 Grade: ");
   double course2Grade = scanner.nextDouble();
   scanner.nextLine();


   // Course 3
   System.out.println("Enter Course 3: ");
   String course3 = scanner.nextLine();
   System.out.println("Enter credit hours for Course 3: ");
   int credit3 = scanner.nextInt();
   System.out.println("Enter Course 3 Grade: ");
   double course3Grade = scanner.nextDouble();
   scanner.nextLine();


   //Course 4
   System.out.println("Enter Course 4: ");
   String course4 = scanner.nextLine();
   System.out.println("Enter credit hours for Course 4: ");
   int credit4 = scanner.nextInt();
   System.out.println("Enter Course 4 Grade: ");
   double course4Grade  = scanner.nextDouble();
   scanner.nextLine();


   //Course 5
   System.out.println("Enter Course 5:");
   String course5 = scanner.nextLine();
   System.out.println("Enter credit hours for Course 5: ");
   int credit5 = scanner.nextInt();
   System.out.println("Enter Course 5 Grade: ");
   double course5Grade = scanner.nextDouble();
   scanner.nextLine();


   double average = (course1Grade + course2Grade + course3Grade + course4Grade + course5Grade) / 5;
   double totalWeightedGrade = (course1Grade * credit1 + course2Grade * credit2 + course3Grade * credit3 + course4Grade * credit4 + course5Grade * credit5);
   int totalCredits = credit1 + credit2 + credit3 + credit4 + credit5;
   double weightedAverage = totalWeightedGrade / totalCredits;


   System.out.println("Average Grade: " + average);
   System.out.println("Weighted GPA: " + weightedAverage);
   System.out.println("Total Credits: " + totalCredits);


   String letterGrade;
   if (average >= 90){
       letterGrade = "A";
   } else if (average >= 80){
       letterGrade = "B";
   } else if (average >= 70){
       letterGrade = "C";
   } else if (average >= 60){
       letterGrade = "D";
   } else {
       letterGrade = "F";
   }


   Student student = new Student(name, id, course1, course2, course3, course4, course5);


   System.out.println("\\\\ STUDENT GRADE REPORT ////");
   System.out.println("Student Name: " + student.name);
   System.out.println("Enter Student ID: " + student.id);
   System.out.println("Enter Course 1: " + student.course1 + " Grade: " + course1Grade);
   System.out.println("Enter Course 2: " + student.course2 + " Grade: " + course2Grade);
   System.out.println("Enter Course 3: " + student.course3 + " Grade: " + course3Grade);
   System.out.println("Enter Course 4: " + student.course4 + " Grade: " + course4Grade);
   System.out.println("Enter Course 5: " + student.course5 + " Grade: " + course5Grade);
   System.out.println("Weighted GPA: " + weightedAverage);
   System.out.println("Total Credits: " + totalCredits);
   System.out.println("Final Letter Grade: " + letterGrade);
   }
   }


class Student{
   String name;
   int id;
   String course1;
   String course2;
   String course3;
   String course4;
   String course5;


   public Student(String name, int id, String course1, String course2, String course3, String course4, String course5){
       this.name = name;
       this.id = id;
       this.course1 = course1;
       this.course2 = course2;
       this.course3 = course3;
       this.course4 = course4;
       this.course5 = course5;


   }
}
