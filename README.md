# Hollow Right-Angled Triangle Pattern in Java

## Introduction
This Java program prints a **hollow right-angled triangle** pattern using the `*` (asterisk) symbol. The user provides the size of the triangle, and the program generates the pattern based on the given input.

### Example Output for n = 5
```
Enter the Size: 5
*
**
* *
*  *
*****
```

## Code
```java
package star_patterns;

import java.util.Scanner;

public class Hollw_RightAngle_Triangle
{
    public static void main(String[] args)
    {
        Scanner s = new Scanner(System.in);
        System.out.println("Enter the Size");
        int n = s.nextInt();
        for(int i=1; i<=n; i++)
        {
            for(int j=1; j<=i; j++)
            {
                if(j==1 || i==n || j==i)
                    System.out.print("*");
                else
                    System.out.print(" ");
            }
            System.out.println();
        }
    }
}
```

---

## Explanation
### 1. **Scanner Class**
The program uses `Scanner` to take input from the user:
```java
Scanner s = new Scanner(System.in);
```
- `Scanner` is a Java utility class used to take user input.
- `System.in` allows the program to read input from the console.
- `s.nextInt()` reads an integer from the user and stores it in `n`.

### 2. **Variables Used**
- `int n`: Stores the size of the triangle (user input).
- `int i, j`: Loop variables used to control row (`i`) and column (`j`) iterations.

### 3. **For Loop (Outer Loop)**
The outer `for` loop runs from `1` to `n`, controlling the rows:
```java
for(int i=1; i<=n; i++)
```
- Starts from `i = 1` (first row) and goes up to `n` (last row).
- Controls how many rows will be printed.

### 4. **Nested For Loop (Inner Loop)**
The inner `for` loop runs from `1` to `i`, controlling the columns:
```java
for(int j=1; j<=i; j++)
```
- Controls the number of characters printed in each row.
- Ensures that each row contains `i` characters.

### 5. **Conditional Statements**
Inside the inner loop, an `if` condition decides whether to print `*` or a space:
```java
if(j==1 || i==n || j==i)
    System.out.print("*");
else
    System.out.print(" ");
```
- `j==1`: Ensures that the first column always has `*`.
- `i==n`: Ensures that the last row is filled with `*`.
- `j==i`: Ensures that the last column of each row has `*`.
- `else`: Prints a space (` `) for the hollow part of the triangle.

### 6. **Printing Statements**
- `System.out.print("*")`: Prints `*` without moving to the next line.
- `System.out.print(" ")`: Prints a space without moving to the next line.
- `System.out.println()`: Moves to the next line after completing each row.

---

## Pattern Breakdown (Step-by-Step Execution)
For `n = 5`:

| Row (i) | Printed Characters (j) |
|---------|------------------------|
| 1       | `*`                    |
| 2       | `**`                   |
| 3       | `* *`                  |
| 4       | `*  *`                 |
| 5       | `*****`                |

---

## Conclusion
This program demonstrates:
- **Usage of `Scanner`** to take user input.
- **For loops** for row and column iterations.
- **Conditional statements** to print `*` or space.
- **Printing techniques** using `System.out.print()` and `System.out.println()`.

## Clone
```
git clone https://github.com/Ananthadatta02/Java-Hollw_RightAngle_Triangle.git
```
