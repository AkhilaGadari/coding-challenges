# Day 01 – Unstop 100 Days Coding Challenge
Platform: Unstop  
##Question:1
Problem Link: https://unstop.com/code/challenge-assessment/250904?moduleId=372  

Time Complexity: O(1)  
Space Complexity: O(1)

## Solution
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







 
##Question:2
Problem Link: https://unstop.com/code/challenge-assessment/250196?moduleId=372

Time Complexity: O(n + m) 
Space Complexity: O(n + m)

## Solution


import java.util.*;

public class Main {
    public static void find_youngest_member(int n, int m, int[][] gifts) {
       
        int[] giver=new int[n+1];
        int[] receive=new int[n+1];
        for(int i=0;i<m;i++){
            int a=gifts[i][0];
            int b=gifts[i][1];

            giver[a]++;
            receive[b]++;

        }
        for(int i=1;i<=n;i++){
            if(giver[i]==0 && receive[i]==n-1){
               System.out.println(i);
               return;
            }
           

        }
         System.out.println(-1);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int m = scanner.nextInt();
        int[][] gifts = new int[m][2];
        for (int i = 0; i < m; i++) {
            gifts[i][0] = scanner.nextInt();
            gifts[i][1] = scanner.nextInt();
        }
        find_youngest_member(n, m, gifts);
    }
}



##Question:3
Problem Link: https://unstop.com/code/challenge-assessment/250739?moduleId=372

Time Complexity: O(n) 
Space Complexity: O(n)

## Solution

import java.util.*;

class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int N = sc.nextInt();
        String[] arr = new String[N];

        for(int i = 0; i < N; i++){
            arr[i] = sc.next();
        }

        int k = sc.nextInt();

        HashMap<String,Integer> map = new HashMap<>();


        for(String s : arr){
            map.put(s, map.getOrDefault(s,0) + 1);
        }

        int count = 0;

        for(String s : arr){
            if(map.get(s) == 1){
                count++;
                if(count == k){
                    System.out.println(s);
                    return;
                }
            }
        }

        System.out.println(-1);
    }
}
