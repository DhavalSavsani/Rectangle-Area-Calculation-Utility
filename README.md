# Rectangle-Area-Calculation-Utility

/*
 * Rectangle Area Calculation Utility
 * This program reads the length and breadth of a rectangle from user input
 * and calculates the area.
 */

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Final {

    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            System.out.println("Enter the length :- ");
            int length = Integer.parseInt(br.readLine());
            System.out.println("Enter the breadth :- ");
            int breadth = Integer.parseInt(br.readLine());
            
            Area area = new Area(length, breadth);
            System.out.println("The Area of rectangle is " + area.getArea());
        } catch (IOException e) {
            System.err.println("Error reading input: " + e.getMessage());
        } catch (NumberFormatException e) {
            System.err.println("Invalid input. Please enter integers for length and breadth.");
        } catch (Exception e) {
            System.err.println("An unexpected error occurred: " + e.getMessage());
        }
    }
}
