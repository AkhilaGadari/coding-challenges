# Day 01 – Unstop 100 Days Coding Challenge
Platform: Unstop  
Problem Link: https://unstop.com/code/challenge-assessment/250904?moduleId=372  

Time Complexity: O(1)  
Space Complexity: O(1)

## Solution (Java)
import java.util.Scanner;

public class Main {

    public static String determineColor(String s) {
        return ((s.charAt(0) + s.charAt(1)) % 2 == 0) ? "Black" : "White";
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String s = scanner.nextLine().trim();
        String result = determineColor(s);
        System.out.println(result);
    }
}

