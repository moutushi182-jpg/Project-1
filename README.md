# Project-1
Calculator
#include <stdio.h>

int main() {
    char operator;
    double num1, num2;

    // Input from user
    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator);  // Notice the space before %c to ignore any leftover whitespace
    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);

    // Perform calculation
    switch(operator) {
        case '+':
            printf("%.2lf + %.2lf = %.2lf\n", num1, num2, num1 + num2);
            break;
        case '-':
            printf("%.2lf - %.2lf = %.2lf\n", num1, num2, num1 - num2);
            break;
        case '*':
            printf("%.2lf * %.2lf = %.2lf\n", num1, num2, num1 * num2);
            break;
        case '/':
            if(num2 != 0)
                printf("%.2lf / %.2lf = %.2lf\n", num1, num2, num1 / num2);
            else
                printf("Error! Division by zero.\n");
            break;
        default:
            printf("Invalid operator.\n");
    }

    return 0;
}
