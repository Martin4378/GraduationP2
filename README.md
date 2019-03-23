# GraduationP2

import java.util.Scanner;

public class P47_GraduationP2 {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        String name = scanner.nextLine();
        int grade = 1;
        double averageGrade = 0;
        int lowGradeCounter = 0;

        while (grade <= 12){

            double grademark = Double.parseDouble(scanner.nextLine());

            if (grademark >= 4.00){
                grade++;
                averageGrade += grademark / 12;
            }
            else {
                lowGradeCounter ++;
            }
            if (grade > 12) {
                System.out.printf("%s graduated. Average grade: %.2f", name, averageGrade);
            }
            else if (lowGradeCounter > 1){
                System.out.printf("%s has been excluded at %d grade", name, grade);
                break;
            }

        }


    }

}
