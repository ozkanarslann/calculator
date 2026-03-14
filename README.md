#include <stdio.h>

int main() {
    char operator;
    double num1, num2;

    printf("Calculator Program\n");
    printf("Choose an operation (+, -, *, /): ");
    scanf(" %c", &operator);

    printf("Enter the first number: ");
    scanf("%lf", &num1);
    printf("Enter the second number: ");
    scanf("%lf", &num2);

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
                printf("Error: Division by zero is undefined!\n");
            break;
        default:
            printf("Error: Invalid operation!\n");
    }

    return 0;
}
