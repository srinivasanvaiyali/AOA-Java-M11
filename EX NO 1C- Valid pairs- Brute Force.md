## EX 1C Valid Pairs using Brute Force Approach
# DATE:
# AIM:
To write a Java program to for given constraints. Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0. -x if x < 0.

# Algorithm
1.Start the program and read the integer input n (array size), the array elements nums[], and the integer k.

2.Initialize a variable count to 0 to store the number of valid pairs.

3.Use two nested loops to check all possible pairs (i, j) where i < j.

4.For each pair, calculate |nums[i] - nums[j]|;

5.If the result equals k, increment the count by 1.

6.After checking all pairs, print the value of count and stop the program

# Program:
```

Program to implement Reverse a String
Developed by: SRINIVASAN V
Register Number:212222043008
```
```

import java.util.Scanner;
public class CountPairsWithDifference {
    public static int countKDifference(int[] nums, int k) {
        int count=0;
        for (int i=0;i<nums.length;i++){
            for (int j=i+1;j<nums.length;j++){
                if(Math.abs(nums[i]-nums[j])==k){
                    count++;
                }
            }
        }
        //Type your code here
        return count;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int result = countKDifference(nums, k);
        System.out.println(result);
        sc.close();
    }
}
```
# OUTPUT :
<img width="627" height="324" alt="512106718-7308b6af-8317-4321-ba72-dba342c99ff4" src="https://github.com/user-attachments/assets/f4a795a2-695a-4248-a7d5-52a52d0cf09b" />

# Result:
The program successfully implemented and the expected output is verified.

