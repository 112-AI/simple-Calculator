# simple-Calculator

package adi3;

import java.util.Scanner;

public class adi3 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter a value for 'a': ");
        int a = scanner.nextInt();
        
        
        generateSeries(a);
        
        scanner.close();
    }

    public static void generateSeries(int a) {
        if (a <= 0) {
            System.out.println("Invalid input. Please enter a positive integer.");
            return;
        }
        
        
        int seriesLength = (a % 2 == 0) ? a - 1 : a;

        
        StringBuilder series = new StringBuilder();
        for (int i = 1; i <= seriesLength; i += 2) {
            series.append(i).append(", ");
        }
        
        if (series.length() > 0) {
            series.setLength(series.length() - 2);
        }
        
        System.out.println("Output: " + series.toString());
    }
}



its a java code
