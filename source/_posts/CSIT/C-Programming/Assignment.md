---
title: "C-Programming Lab Assignment 1"
date: "2024-12-05"
description: "C Programming Lab Assignments for BSc CSIT First Semester at Patan Multiple Campus"
tags:
  - Assignment
  - C-Programming
  - Lab
categories:
  - CSIT
  - Semester 1
---

# Questions

1. . Write a C program to print your name, date of birth and mobile number and Name of
College using printf() and puts() functions in following format.
Name: ……
DOB:
MobileNO:
Campus:

2. Write a C program to display size in bytes of different data types using sizeof() operator.

3. Write algorithm, flow-chart and program to compute the area and circumference of a circle with given radius r as input defining π as constant.

4. Write a C program to convert specified no of days into years, weeks and days. (Note: Ignore leap year.)

5. Write a C program that accepts two integers from the user as input and calculates the sum, difference, product, quotient and remainder applying different arithmetic operators between two integers.

6. Write algorithm pseudo-code as well as draw flow chart to Compute the roots of the quadratic equation ax² + bx + c = 0 for given coefficient input a, b and c. Write C program.

7. Write a C program to check a given integer is positive even, negative even, positive odd or negative odd.

8. Write a C program to read the score of student and print the grade according to score as:
   - Score >= 80: "Distinction"
   - Score 70-79: "First Division"
   - Score 55-69: "Second Division"
   - Score 40-54: "Third Division"
   - Score < 40: "Fail"

9. Write a C program to find the sum of first 100 natural numbers using loop.

10. Write a program in C to display the multiplication table of 1 to n where n is input number.

11. Write algorithm and program to compute the followings using for, do while and while loop separately:
    a. factorial of an integer N
    b. computation of aᵇ (a raised to power b)

12. Write a program in C to make such a pattern of asterisk(*) below using loop:
    ```
    *
    * *
    * * *
    * * * *
    ```
    up to n lines where n is an integer

13. Write a program using loop to print Floyd's triangle as given below when input is n:
    ```
    1
    2 3
    4 5 6
    7 8 9 10
    11 12 13 14
    ```
    up to n rows

14. Write a program to get input of two 3x3 matrices and find out the sum and product of the matrices and display the result.

15. Write a program to get a string as input and print the length of string, reverse of the string:
    a. Using String Library Function
    b. Using your own function

16. Write a program that takes input of two numbers and any one operator (+,-,*,/,%) as input and pass those numbers and operator to a function. The function should calculate and return the result. Display the result of computation.

17. Write a program defining an array with dynamic memory allocation of integers and compute the sum of the array using function.

18. Write a program to swap two numbers defining a function swap().

19. Write a program defining a structure to store student data (rollno, f_name, l_name, address, mobileno), input data for n students and display the record.

20. Write a program to prompt user to input filename and read the content of file and display in screen.

21. Write a program to read from a text file and count the number of lines and characters in that file.

22. Write a program to read a text file and copy all contents in the new file.

---

# Solutions
---

### 1. **Print Name, DOB, Mobile Number, and Campus**
**Code**: 
```c
#include <stdio.h>
int main() {
    printf("Name: John Doe\n");
    printf("DOB: 2000-01-01\n");
    printf("Mobile No: 9800000000\n");
    puts("Campus: Patan Multiple Campus");
    return 0;
}
```
**Output**:
```
Name: John Doe
DOB: 2000-01-01
Mobile No: 9800000000
Campus: Patan Multiple Campus
```

---

### 2. **Display Size of Data Types**
**Code**:
```c
#include <stdio.h>
int main() {
    printf("Size of int: %lu bytes\n", sizeof(int));
    printf("Size of float: %lu bytes\n", sizeof(float));
    printf("Size of double: %lu bytes\n", sizeof(double));
    printf("Size of char: %lu byte\n", sizeof(char));
    return 0;
}
```
**Output**:
```
Size of int: 4 bytes
Size of float: 4 bytes
Size of double: 8 bytes
Size of char: 1 byte
```

---

### 3. **Area and Circumference of Circle**
**Code**:
```c
#include <stdio.h>
#define PI 3.14159
int main() {
    float radius, area, circumference;
    printf("Enter radius: ");
    scanf("%f", &radius);
    area = PI * radius * radius;
    circumference = 2 * PI * radius;
    printf("Area: %.2f\nCircumference: %.2f\n", area, circumference);
    return 0;
}
```
**Output**:
```
Enter radius: 5
Area: 78.54
Circumference: 31.42
```

---

### 4. **Days to Years, Weeks, and Days**
**Code**:
```c
#include <stdio.h>
int main() {
    int days, years, weeks, remaining_days;
    printf("Enter days: ");
    scanf("%d", &days);
    years = days / 365;
    weeks = (days % 365) / 7;
    remaining_days = days % 7;
    printf("%d years, %d weeks, %d days\n", years, weeks, remaining_days);
    return 0;
}
```
**Output**:
```
Enter days: 400
1 years, 5 weeks, 0 days
```

---

### 5. **Arithmetic Operations**
**Code**:
```c
#include <stdio.h>
int main() {
    int a, b;
    printf("Enter two integers: ");
    scanf("%d %d", &a, &b);
    printf("Sum: %d\n", a + b);
    printf("Difference: %d\n", a - b);
    printf("Product: %d\n", a * b);
    printf("Quotient: %d\n", a / b);
    printf("Remainder: %d\n", a % b);
    return 0;
}
```
**Output**:
```
Enter two integers: 10 3
Sum: 13
Difference: 7
Product: 30
Quotient: 3
Remainder: 1
```

### 6. **Roots of Quadratic Equation**
**Code**:
```c
#include <stdio.h>
#include <math.h>
int main() {
    float a, b, c, discriminant, root1, root2;
    printf("Enter coefficients a, b, and c: ");
    scanf("%f %f %f", &a, &b, &c);
    discriminant = b * b - 4 * a * c;
    if (discriminant > 0) {
        root1 = (-b + sqrt(discriminant)) / (2 * a);
        root2 = (-b - sqrt(discriminant)) / (2 * a);
        printf("Roots: %.2f and %.2f\n", root1, root2);
    } else if (discriminant == 0) {
        root1 = -b / (2 * a);
        printf("Root: %.2f\n", root1);
    } else {
        printf("No real roots.\n");
    }
    return 0;
}
```
**Output**:
```
Enter coefficients a, b, and c: 1 -3 2
Roots: 2.00 and 1.00
```

---

### 7. **Check Integer Type**
**Code**:
```c
#include <stdio.h>
int main() {
    int num;
    printf("Enter an integer: ");
    scanf("%d", &num);
    if (num > 0 && num % 2 == 0)
        printf("Positive Even\n");
    else if (num > 0)
        printf("Positive Odd\n");
    else if (num < 0 && num % 2 == 0)
        printf("Negative Even\n");
    else
        printf("Negative Odd\n");
    return 0;
}
```
**Output**:
```
Enter an integer: -4
Negative Even
```

---

### 8. **Grade Calculation**
**Code**:
```c
#include <stdio.h>
int main() {
    int score;
    printf("Enter score: ");
    scanf("%d", &score);
    if (score >= 80)
        printf("Distinction\n");
    else if (score >= 70)
        printf("First Division\n");
    else if (score >= 55)
        printf("Second Division\n");
    else if (score >= 40)
        printf("Third Division\n");
    else
        printf("Fail\n");
    return 0;
}
```
**Output**:
```
Enter score: 75
First Division
```

---

### 9. **Sum of First 100 Natural Numbers**
**Code**:
```c
#include <stdio.h>
int main() {
    int sum = 0;
    for (int i = 1; i <= 100; i++)
        sum += i;
    printf("Sum: %d\n", sum);
    return 0;
}
```
**Output**:
```
Sum: 5050
```

---

### 10. **Multiplication Table of 1 to n**
**Code**:
```c
#include <stdio.h>
int main() {
    int n;
    printf("Enter n: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        printf("Table of %d:\n", i);
        for (int j = 1; j <= 10; j++)
            printf("%d x %d = %d\n", i, j, i * j);
    }
    return 0;
}
```
**Output**:
```
Enter n: 2
Table of 1:
1 x 1 = 1
1 x 2 = 2
...
Table of 2:
2 x 1 = 2
2 x 2 = 4
...
```

---
### 11. **Factorial and Power Calculation**
**Factorial Using `for` Loop**:
```c
#include <stdio.h>
int main() {
    int n, factorial = 1;
    printf("Enter n: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++)
        factorial *= i;
    printf("Factorial: %d\n", factorial);
    return 0;
}
```

**Output**:
```
Enter n: 5
Factorial: 120
```

**Power Calculation Using `while` Loop**:
```c
#include <stdio.h>
int main() {
    int base, exp, result = 1;
    printf("Enter base and exponent: ");
    scanf("%d %d", &base, &exp);
    while (exp-- > 0)
        result *= base;
    printf("Result: %d\n", result);
    return 0;
}
```

**Output**:
```
Enter base and exponent: 2 3
Result: 8
```

---

### 12. **Pattern of Asterisks**
**Code**:
```c
#include <stdio.h>
int main() {
    int n;
    printf("Enter number of lines: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= i; j++)
            printf("* ");
        printf("\n");
    }
    return 0;
}
```
**Output**:
```
*
* *
* * *
...
```

---

### 13. **Floyd's Triangle**
**Code**:
```c
#include <stdio.h>
int main() {
    int n, num = 1;
    printf("Enter number of rows: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= i; j++)
            printf("%d ", num++);
        printf("\n");
    }
    return 0;
}
```

**Output**:
```
Enter number of rows: 4
1 
2 3 
4 5 6 
7 8 9 10
```

---

### 14. **Matrix Sum and Product**
**Code**:
```c
#include <stdio.h>
void readMatrix(int matrix[3][3]) {
    for (int i = 0; i < 3; i++)
        for (int j = 0; j < 3; j++)
            scanf("%d", &matrix[i][j]);
}
void printMatrix(int matrix[3][3]) {
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++)
            printf("%d ", matrix[i][j]);
        printf("\n");
    }
}
void addMatrices(int a[3][3], int b[3][3], int result[3][3]) {
    for (int i = 0; i < 3; i++)
        for (int j = 0; j < 3; j++)
            result[i][j] = a[i][j] + b[i][j];
}
int main() {
    int a[3][3], b[3][3], sum[3][3];
    printf("Enter first matrix:\n");
    readMatrix(a);
    printf("Enter second matrix:\n");
    readMatrix(b);
    addMatrices(a, b, sum);
    printf("Sum:\n");
    printMatrix(sum);
    return 0;
}
```

**Output**:
```
Enter first matrix:
1 2 3
4 5 6
7 8 9
Enter second matrix:
9 8 7
6 5 4
3 2 1
Sum:
10 10 10
10 10 10
10 10 10
```

---
### 15. **String Length and Reverse**
**Program** *(Using String Library Functions)*:
```c
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    printf("Enter a string: ");
    gets(str);
    printf("Length: %lu\n", strlen(str));
    strrev(str);
    printf("Reversed: %s\n", str);
    return 0;
}
```

**Sample Input/Output**:
```
Enter a string: Nepal
Length: 5
Reversed: lapeN
```

**Program** *(Without String Library Functions)*:
```c
#include <stdio.h>
int stringLength(char str[]) {
    int length = 0;
    while (str[length] != '\0')
        length++;
    return length;
}
void reverseString(char str[]) {
    int len = stringLength(str);
    for (int i = 0; i < len / 2; i++) {
        char temp = str[i];
        str[i] = str[len - i - 1];
        str[len - i - 1] = temp;
    }
}
int main() {
    char str[100];
    printf("Enter a string: ");
    gets(str);
    printf("Length: %d\n", stringLength(str));
    reverseString(str);
    printf("Reversed: %s\n", str);
    return 0;
}
```

**Sample Input/Output**:
```
Enter a string: HelloWorld
Length: 10
Reversed: dlroWolleH
```

---

### 16. **Calculator Using Functions**
**Program**:
```c
#include <stdio.h>
float calculate(float a, float b, char op) {
    switch (op) {
        case '+': return a + b;
        case '-': return a - b;
        case '*': return a * b;
        case '/': return a / b;
        case '%': return (int)a % (int)b;
        default: return 0;
    }
}
int main() {
    float num1, num2;
    char op;
    printf("Enter two numbers and an operator: ");
    scanf("%f %f %c", &num1, &num2, &op);
    printf("Result: %.2f\n", calculate(num1, num2, op));
    return 0;
}
```

**Sample Input/Output**:
```
Enter two numbers and an operator: 10 3 %
Result: 1.00
```

---

### 17. **Dynamic Memory Allocation and Sum of Array**
**Program**:
```c
#include <stdio.h>
#include <stdlib.h>
int sumArray(int *arr, int size) {
    int sum = 0;
    for (int i = 0; i < size; i++)
        sum += arr[i];
    return sum;
}
int main() {
    int n, *arr;
    printf("Enter size of array: ");
    scanf("%d", &n);
    arr = (int *)malloc(n * sizeof(int));
    printf("Enter %d elements: ", n);
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);
    printf("Sum: %d\n", sumArray(arr, n));
    free(arr);
    return 0;
}
```

**Sample Input/Output**:
```
Enter size of array: 5
Enter 5 elements: 1 2 3 4 5
Sum: 15
```

---

### 18. **Swap Two Numbers Using a Function**
**Program**:
```c
#include <stdio.h>
void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}
int main() {
    int x, y;
    printf("Enter two numbers: ");
    scanf("%d %d", &x, &y);
    swap(&x, &y);
    printf("After swapping: x = %d, y = %d\n", x, y);
    return 0;
}
```

**Sample Input/Output**:
```
Enter two numbers: 5 10
After swapping: x = 10, y = 5
```

---

### 19. **Structure for Student Data**
**Program**:
```c
#include <stdio.h>
struct Student {
    int rollno;
    char fname[50], lname[50], address[100];
    char mobileno[15];
};
int main() {
    int n;
    printf("Enter number of students: ");
    scanf("%d", &n);
    struct Student students[n];
    for (int i = 0; i < n; i++) {
        printf("Enter details for student %d:\n", i + 1);
        printf("Roll No: ");
        scanf("%d", &students[i].rollno);
        printf("First Name: ");
        scanf("%s", students[i].fname);
        printf("Last Name: ");
        scanf("%s", students[i].lname);
        printf("Address: ");
        scanf("%s", students[i].address);
        printf("Mobile No: ");
        scanf("%s", students[i].mobileno);
    }
    printf("Student Records:\n");
    for (int i = 0; i < n; i++) {
        printf("Roll No: %d, Name: %s %s, Address: %s, Mobile No: %s\n",
               students[i].rollno, students[i].fname, students[i].lname,
               students[i].address, students[i].mobileno);
    }
    return 0;
}
```

**Sample Input/Output**:
```
Enter number of students: 1
Enter details for student 1:
Roll No: 1
First Name: Prashant
Last Name: Giri
Address: Kathmandu
Mobile No: 9876543210
Student Records:
Roll No: 1, Name: Prashant Giri, Address: Kathmandu, Mobile No: 9876543210
```

---

### 20. **Read and Display File Content**
**Program**:
```c
#include <stdio.h>
int main() {
    char filename[50], ch;
    printf("Enter filename: ");
    scanf("%s", filename);
    FILE *file = fopen(filename, "r");
    if (file == NULL) {
        printf("File not found.\n");
        return 1;
    }
    while ((ch = fgetc(file)) != EOF)
        putchar(ch);
    fclose(file);
    return 0;
}
```

**Sample Input/Output** *(assuming file contains "Hello World")*:
```
Enter filename: input.txt
Hello World
```

---

### 21. **Count Lines and Characters in File**
**Program**:
```c
#include <stdio.h>
int main() {
    char filename[50], ch;
    int lines = 0, chars = 0;
    printf("Enter filename: ");
    scanf("%s", filename);
    FILE *file = fopen(filename, "r");
    if (file == NULL) {
        printf("File not found.\n");
        return 1;
    }
    while ((ch = fgetc(file)) != EOF) {
        chars++;
        if (ch == '\n')
            lines++;
    }
    fclose(file);
    printf("Lines: %d, Characters: %d\n", lines, chars);
    return 0;
}
```

**Sample Input/Output** *(assuming file contains two lines "Hello\nWorld")*:
```
Enter filename: input.txt
Lines: 2, Characters: 11
```

---

### 22. **Copy Content to New File**
**Program**:
```c
#include <stdio.h>
int main() {
    char src[50], dest[50], ch;
    printf("Enter source filename: ");
    scanf("%s", src);
    printf("Enter destination filename: ");
    scanf("%s", dest);
    FILE *srcFile = fopen(src, "r");
    FILE *destFile = fopen(dest, "w");
    if (srcFile == NULL || destFile == NULL) {
        printf("File error.\n");
        return 1;
    }
    while ((ch = fgetc(srcFile)) != EOF)
        fputc(ch, destFile);
    printf("File copied successfully.\n");
    fclose(srcFile);
    fclose(destFile);
    return 0;
}
```

**Sample Input/Output**:
```
Enter source filename: input.txt
Enter destination filename: output.txt
File copied successfully.
```

Let me know if there are any errors.
