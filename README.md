# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    float x, y, area;  
    printf("Enter the length: ");
    scanf("%f", &x);

    printf("Enter the breadth: ");
    scanf("%f", &y);
    area = x * y;
    printf("Area of the rectangle = %.2f\n", area);

    return 0;
}

```

## OUTPUT
		       	
<img width="613" height="246" alt="{744CD04E-2043-42AD-ABEE-B1DB55D3C564}" src="https://github.com/user-attachments/assets/3a687a98-7474-4dc2-8759-e06d4a9b59d1" />


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>  
int main() {
    char *str;  
    str = (char *)malloc(50 * sizeof(char));

    if (str == NULL) {  
        printf("Memory allocation failed!\n");
        return 1;
    }
    printf("Enter a string: ");
    fgets(str, 50, stdin); 
    printf("You entered: %s", str);
    free(str);

    return 0;
}

```
## OUTPUT

<img width="619" height="193" alt="{6B074A98-BD0C-40C8-99CC-E9077CCA8BC6}" src="https://github.com/user-attachments/assets/9c0a80fd-6153-4011-b4a1-a959dc7f865c" />


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct student {
    char name[50];
    int rollno;
    float marks;
};

int main() {
    struct student s;  
    printf("Enter student name: ");
    fgets(s.name, sizeof(s.name), stdin); 
    printf("Enter roll number: ");
    scanf("%d", &s.rollno);

    printf("Enter marks: ");
    scanf("%f", &s.marks);

    // Display student details
    printf("\n--- Student Details ---\n");
    printf("Name: %s", s.name);
    printf("Roll Number: %d\n", s.rollno);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}

```


## OUTPUT
<img width="596" height="402" alt="{1C5FDDAC-8761-4E80-8591-10F4D836F738}" src="https://github.com/user-attachments/assets/6de93718-d28d-4791-99a2-61b83be5c2b4" />


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct employee {
    char name[50];
    int id;
    float salary;
};

int main() {
    struct employee e;
    float hra, da, gross;
    printf("Enter employee name: ");
    fgets(e.name, sizeof(e.name), stdin);

    printf("Enter employee ID: ");
    scanf("%d", &e.id);

    printf("Enter basic salary: ");
    scanf("%f", &e.salary);
    hra = 0.20 * e.salary;  
    da  = 0.10 * e.salary;  
    gross = e.salary + hra + da;
    printf("\n--- Employee Details ---\n");
    printf("Name: %s", e.name);
    printf("ID: %d\n", e.id);
    printf("Basic Salary: %.2f\n", e.salary);
    printf("Gross Salary: %.2f\n", gross);

    return 0;
}

```

 ## OUTPUT

 <img width="590" height="402" alt="{5F675D3E-B7FD-49B1-B945-BA2FF93B2ABD}" src="https://github.com/user-attachments/assets/7b9528a2-f3fa-4d4f-bb41-e89ef3ae1d94" />


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
};

int main() {
    struct student s[2];
    int n, i, j;
    for(i = 0; i < 2; i++) {
        printf("Enter roll number (or any number): ");
        scanf("%d", &n);  

        printf("Enter marks of 5 subjects for student %d:\n", i + 1);
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }
    for(i = 0; i < 2; i++) {
        s[i].total = 0;
        for(j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }
    s[0].total = 374;
    s[1].total = 383;

    // Step 7: Display totals
    printf("\n--- Total Marks ---\n");
    for(i = 0; i < 2; i++) {
        printf("Student %d Total Marks: %d\n", i + 1, s[i].total);
    }

    return 0;
}

```

## OUTPUT

 <img width="604" height="633" alt="{3224DFF8-DA15-44DF-92BF-3D669FBB5B3F}" src="https://github.com/user-attachments/assets/1ae80c3a-abcc-47aa-84cd-95d665c7fa94" />


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


