# java-strong-number
A simple Java program to check and print Strong Numbers (numbers equal to the sum of the factorial of their digits).
import java.util.*;
public class StrongNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int original = a; 
        int sum = 0;

        while (a != 0) {
            int temp = a % 10;
            int fact = 1;
            for (int i = 1; i <= temp; i++) {
                fact = fact * i;
            }
            sum = sum + fact;
            a = a / 10;
        }

        if (sum == original) {
            System.out.println(original + " is a Strong Number");
        } else {
            System.out.println(original + " is not a Strong Number");
        }
    }
}

