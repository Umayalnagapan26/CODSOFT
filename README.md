FIRST TASK IN CODSOFT:

STUDENT GRADE CALCULATOR

Input: Take marks obtained (out of 100) in each subject.
Calculate Total Marks: Sum up the marks obtained in all subjects.
Calculate Average Percentage: Divide the total marks by the total number of subjects to get the
average percentage.
Grade Calculation: Assign grades based on the average percentage achieved.
Display Results: Show the total marks, average percentage, and the corresponding grade to the user 

PROGRAM:
import java.util.Scanner;
public class Markt
{
public static void main(String[] args) 
{
      Scanner s = new Scanner(System.in);
      System.out.print("Enter the number of subjects: ");
      int nSub = s.nextInt();
      int marks[] = new int[nSub];

       
        for (int i = 0; i < nSub; i++) {
        System.out.printf("Enter marks obtained in subject %d (out of 100): ", i + 1);
        marks[i] = s.nextInt();
        }

       
        int totalMarks = 0;
        for (int mark : marks) {
            totalMarks =totalMarks + mark;
        }

       double average= (double) totalMarks / nSub;

        char grade;
        if (average >= 90) {
            grade = 'A';
        } else if (average < 90 && average>=80) {
            grade = 'B';
        } else if (average < 80 && average>=70) {
            grade = 'C';
        } else if (average < 70 && average>=60) {
            grade = 'D';
        } else {
            grade = 'F'; 
        }

        
        System.out.println("Results:");
        System.out.println("Total Marks: " + totalMarks);
        System.out.printf("Average Percentage: %.2f%%\n", average);
        System.out.println("Grade: " + grade);

      
    }
}

OUTPUT:
Enter the number of subjects: 5
Enter marks obtained in subject 1 (out of 100): 98
Enter marks obtained in subject 2 (out of 100): 99
Enter marks obtained in subject 3 (out of 100): 89
Enter marks obtained in subject 4 (out of 100): 97
Enter marks obtained in subject 5 (out of 100): 78
Results:
Total Marks: 461
Average Percentage: 92.20%
Grade: A

