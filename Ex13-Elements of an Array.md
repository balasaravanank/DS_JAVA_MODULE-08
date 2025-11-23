# Ex13 Fill the First 10 Elements of an Array with a Constant using Arrays.fill()
## DATE: 23.11.2025
## AIM:
To write a Java program that fills the first 10 elements of an array with a constant value using the Arrays.fill() method.
## Algorithm
1. Start the program.
2. Read an integer value from the user.
3. Call the function fillArray(10, value).
4. Create an integer array arr of length size.
5. Fill every element of arr with value using Arrays.fill(arr, value).
6. Return the filled array.
7. Store the returned array in arr.
8. Print the message "Array elements:".
9. For each element in arr, print the element.
10. End the program.   

## Program:
```java
/*
Program to FILL the first 10 elements of an array with a constant value using the Arrays.fill() method.
Developed by: BALA SARAVANAN K
RegisterNumber: 212224230031
*/

import java.util.*;

public class FillArrayUsingArraysFill {

    public static int[] fillArray(int size, int value) {
        int[] arr = new int[size];
        Arrays.fill(arr, value);
        return arr;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int value = sc.nextInt();
        int[] arr = fillArray(10, value);
        System.out.println("Array elements:");
        for (int num : arr) {
            System.out.print(num + " ");
        }
        sc.close();
    }
}

```

## Output:

<img width="783" height="387" alt="image" src="https://github.com/user-attachments/assets/7b71119b-0fcd-4cb7-9860-6b99824e0355" />

## Result:
The program successfully fills the first 10 elements of the array with the constant value 5 using the Arrays.fill() method.
