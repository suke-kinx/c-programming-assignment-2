# c-programming-assignment-2
Name:sukesh raja.R
Reg no:212224060268  

1.Write a C program to traverse a 2D matrix and print the values until a negative number is found. Use break statement.
```
#include <stdio.h>
int main() {
int rows, cols;
printf("Enter number of rows and columns: ");
scanf("%d %d", &rows, &cols);
int matrix[rows][cols];
printf("Enter the matrix elements:\n");
for(int i = 0; i < rows; i++) {
for(int j = 0; j < cols; j++) {
scanf("%d", &matrix[i][j]); }
} 
int stop = 0;
printf("Output:\n");
for(int i = 0; i < rows; i++) {
for(int j = 0; j < cols; j++) {
if(matrix[i][j] < 0) {
stop = 1;
break; }
printf("%d ", matrix[i][j]);  }
if(stop == 1) {
break;    }
}

return 0;
}
```
INPUT:
Enter number of rows and columns: 2 3
Enter the matrix elements:

1 2 3

4 -5 6

Output:

1 2 3 4

2.Write a C program to print the numbers from 1 to 100 but avoid printing multiples of 3 and number containing digit 5(5,15,25,35,..). Use continue in the program.
```
#include <stdio.h>
int main()
{
int n;
printf("Enter the limit: ");
scanf("%d", &n);
for(int i = 1; i <= n; i++) {
if(i % 3 == 0) {
continue;}
int temp = i;
int hasFive = 0;
while(temp > 0) {
if(temp % 10 == 5) {
hasFive = 1;
break; }
temp = temp / 10}
if(hasFive) 
continue;}
printf("%d ", i);
}

return 0;
}
```
Enter the limit: 30

Output:

1 2 4 7 8 10 11 13 14 16 17 19 20 22 23 26 28 29

3.Write a C program that performs division of two user inputs and uses goto to handle errors like division by zero or invalid input by redirecting control for re-entry.
```
#include <stdio.h>
int main() {
float a, b, resul
printf("Enter two numbers: ");
if (scanf("%f %f", &a, &b) != 2) {
printf("Invalid input! Try again.\n");
while(getchar() != '\n'); 
goto start;
}
if (b == 0) {
    printf("Error: Division by zero! Try again.\n");
    goto start;
}
result = a / b;
printf("Result = %.2f\n", result);

return 0;
}
```
OUTPUT:

Enter two numbers: 10 0

Error: Division by zero! Try again.

Enter two numbers: a b

Invalid input! Try again.

Enter two numbers: 10 2

Result = 5.00

4.Write a C program for a number guessing game where the loop continues for wrong guesses, breaks on a correct guess, and exits the program using return if the user enters -1.
```
#include<stdio.h> 
int main() {
int guess;
int secret = 5;
while(1) {
    printf("Enter number (-1 to exit): ");
    scanf("%d", &guess);
    if(guess == -1)
        return 0;
if(guess == secret) {
        printf("Correct!\n");
        break;
    }
    printf("Wrong! Try again\n");
}

return 0;
}
```
OUTPUT:

Enter number (-1 to exit): 2

Wrong! Try again

Enter number (-1 to exit): 4

Wrong! Try again

Enter number (-1 to exit): 5

Correct!

5.Write a C program that iterates through an array and, within a loop, uses continue to skip negative elements, break when a zero is encountered,and return to exit the program if an element greater than 100 is found then print the resulting behavior for the array {10, -5, 20, 0, 150, 30}.
```
#include <stdio.h>
int main() {
int arr[6] = {10, -5, 20, 0, 150, 30};
printf("Output:\n");
for(int i = 0; i < 6; i++) {
if(arr[i] < 0) {
continue;
    }
if(arr[i] == 0) {
break; }
if(arr[i] > 100) {
printf("Element > 100 found. Exiting program.\n");

return 0;
    }

    printf("%d ", arr[i]);
}

return 0;
}
```
Output:

10 20
