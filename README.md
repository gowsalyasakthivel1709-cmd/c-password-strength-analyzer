Prepared By: Gowsalya.S
Date: 23.6.26
Introduction
A Password Strength Analyzer is a program that evaluates the strength of a password based on various security criteria. It helps users create strong passwords that are difficult to guess or crack.
Objective
Analyze the strength of a password.
Encourage users to create secure passwords.
Improve cybersecurity awareness.
Features
Checks password length.
Verifies the presence of uppercase letters.
Verifies the presence of lowercase letters.
Checks for numbers.
Checks for special characters.
Classifies passwords as Weak, Medium, or Strong.
Requirements
C Programming Language
GCC Compiler or any C Compiler
Basic knowledge of string handling functions
Algorithm
Input a password from the user.
Check the password length.
Count uppercase letters.
Count lowercase letters.
Count digits.
Count special characters.
Calculate password strength.
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char password[100];
    int upper = 0, lower = 0, digit = 0, special = 0;

    printf("Enter Password: ");
    scanf("%s", password);

    int len = strlen(password);

    for(int i = 0; i < len; i++) {
        if(isupper(password[i]))
            upper++;
        else if(islower(password[i]))
            lower++;
        else if(isdigit(password[i]))
            digit++;
        else
            special++;
    }

    if(len >= 8 && upper > 0 && lower > 0 && digit > 0 && special > 0)
        printf("Strong Password\n");
    else if(len >= 6)
        printf("Medium Password\n");
    else
        printf("Weak Password\n");

    return 0;
}
Display the result as Weak, Medium, or Strong.
Sample C Program
C
Expected Output
Input:
Plain text
Password@123
Output:
Plain text
Strong Password
Advantages
Enhances account security.
Helps users create stronger passwords.
Reduces the risk of unauthorized access.
Conclusion
A Password Strength Analyzer is a useful cybersecurity tool that evaluates password security based on predefined criteria. Strong passwords provide better protection against cyber threats and unauthorized access.
Reviewed By: Decodelabs
