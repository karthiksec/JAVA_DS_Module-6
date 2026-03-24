# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE: 30.1.2026
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Start the program and read the number of sensor readings; store them in an array.

2. Define a recursive function findMin(arr, n) to find the minimum value among the first n elements.

3. Base Case: If only one element exists (n == 1), return that element.

4.  Recursive Case: Compare the last element with the minimum of the remaining elements and return the smaller value.

5.   Call the recursive function with the full array, display the minimum (lowest heartbeat), and stop the program.

## Program:
```java
/**
 * Program: Determine the minimum value (e.g., lowest heartbeat) using recursion
 * Developed by: KARTHIK G
 * Register Number: 212223220043
 */
import java.util.Scanner;

public class MinValueRecursive {
    static int findMin(int arr[], int n) {
        if (n == 1)
            return arr[0];
        return Math.min(arr[n - 1], findMin(arr, n - 1));
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of readings: ");
        int n = sc.nextInt();
        int arr[] = new int[n];
        System.out.println("Enter the readings:");
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();
        System.out.println("Minimum value (lowest heartbeat): " + findMin(arr, n));
        sc.close();
    }
}
```
## OUTPUT
<img width="938" height="161" alt="image" src="https://github.com/user-attachments/assets/4f716123-0d4a-4266-925d-c2fcac272460" />


## Result:
Thus the JAVA program to find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
