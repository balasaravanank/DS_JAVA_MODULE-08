# Ex11 Convert HashSet to ArrayList in Java
## DATE: 23.11.2025
## AIM:
To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
## Algorithm
1. Start the program.
2. Read n
3. Insert elements into a HashSet.
4. Create an ArrayList from the HashSet.
5. Print ArrayList elements.  

## Program:
```java
/*
Program to To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
Developed by: BALA SARAVANAN K
RegisterNumber: 212224230031
*/

import java.util.*;

public class HashSetToArrayList {

    public static ArrayList<Integer> convertToArrayList(HashSet<Integer> set) {
        // Type Your Code Here.
        return new ArrayList<>(set);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        HashSet<Integer> set = new HashSet<>();
        for (int i = 0; i < n; i++) {
            int num = sc.nextInt();
            set.add(num);
        }

        ArrayList<Integer> list = convertToArrayList(set);
        System.out.println("ArrayList contents:");
        for (int num : list) {
            System.out.print(num + " ");
        }
        sc.close();
    }
}

```

## Output:

<img width="611" height="748" alt="image" src="https://github.com/user-attachments/assets/446bb67e-e7e2-4c79-a139-aafbccb144b9" />

## Result:
The program successfully converts a collection of distinct integers stored in a HashSet into an ArrayList

# Ex12 Add Elements from an Array into a TreeSet
## DATE: 23.11.2025
## AIM:
To write a Java program that adds elements from an array into a TreeSet and displays the elements in sorted order.
## Algorithm
1. Read input array
2. Create empty TreeSet
3. Insert all array elements into TreeSet
4. Print TreeSet elements (in sorted order)

## Program:
```java
/*
Program that adds elements from an array into a TreeSet and displays the elements in sorted order.
Developed by: BALA SARAVANAN K
RegisterNumber: 212224230031
*/

import java.util.*;

public class ArrayToTreeSet {

    public static TreeSet<Integer> convertArrayToTreeSet(int[] arr) {
        // Type Your Code Here.
        TreeSet<Integer> set = new TreeSet<>();
        for (int a:arr)
            set.add(a);
        return set;

    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        TreeSet<Integer> treeSet = convertArrayToTreeSet(arr);
        System.out.println("Elements in TreeSet:");
        for (int num : treeSet) {
            System.out.println(num);
        }

        sc.close();
    }
}

```

## Output:

<img width="728" height="633" alt="image" src="https://github.com/user-attachments/assets/22497514-1f81-4585-8cbf-b9b4ddd279ad" />

## Result:
The program successfully adds elements from an array into a TreeSet.


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

# Ex14 Tracking the First Unique Number in a Stream using LinkedHashMap
## DATE: 23.11.2025
## AIM:
To implement a program that tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.

## Algorithm
1. Start the program.
2. Read an integer n (the number of inputs in the stream).
3. Create an empty LinkedHashMap<Integer, Integer> named map.
4. Repeat the following steps for each of the n numbers.
5. After processing all numbers, end the program.
  

## Program:
```java
/*
Program to tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.
Developed by: BALA SARAVANAN K
RegisterNumber: 212224230031
*/

import java.util.*;

public class FirstUniqueNumberStream {

    public static void processStream(int n, Scanner sc) {
        LinkedHashMap<Integer, Integer> map = new LinkedHashMap<>();
        for (int i = 0; i < n; i++) {
            int num = sc.nextInt();
            map.put(num, map.getOrDefault(num, 0) + 1);
            boolean found = false;
            for (Map.Entry<Integer, Integer> entry : map.entrySet()) {
                if (entry.getValue() == 1) {
                    System.out.println("First unique number: " + entry.getKey());
                    found = true;
                    break;
                }
            }
            if (!found) {
                System.out.println("No unique number");
            }
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        processStream(n, sc);
        sc.close();
    }
}

```

## Output:

<img width="860" height="719" alt="image" src="https://github.com/user-attachments/assets/419d5d2f-f551-409c-be4c-d1225fdba393" />

## Result:
The program successfully tracks and returns the first unique number at any point in the integer stream using a LinkedHashMap.


# Ex15 Value Existence Check in a TreeMap
## DATE: 23.11.2025
## AIM:
To write a Java program that checks whether a given value exists in a TreeMap.

## Algorithm
1. Start the program.
2. Create an empty TreeMap<Integer, String> named map.
3. Read an integer.
4. Repeat the following steps for i = 0 to n–1.
5. Read a string.
6. Check whether the value exists in the TreeMap by print.
7.  Stop the program.

## Program:
```java
/*
Program to checks whether a given value exists in a TreeMap.
Developed by: BALA SARAVANAN K
RegisterNumber: 212224230031
*/

import java.util.*;

public class TreeMapValueExistenceCheck {

    public static void checkValue(TreeMap<Integer, String> map, String searchValue) {
        if (map.containsValue(searchValue)) {
            System.out.println("Value \"" + searchValue + "\" exists in the TreeMap.");
        } else {
            System.out.println("Value \"" + searchValue + "\" does not exist in the TreeMap.");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        TreeMap<Integer, String> map = new TreeMap<>();

        int n = sc.nextInt();

        for (int i = 0; i < n; i++) {
            int key = sc.nextInt();
            sc.nextLine();  
            String value = sc.nextLine();
            map.put(key, value);
        }
        String searchValue = sc.nextLine();

        checkValue(map, searchValue);
        sc.close();
    }
}
```

## Output:

<img width="1091" height="793" alt="image" src="https://github.com/user-attachments/assets/f4bd3cf4-c0ae-4991-81d3-2653f1dc3e8e" />

## Result:
Thus, the program successfully checks whether a specified value exists in a TreeMap using the containsValue() method.


