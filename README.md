#include <stdio.h>

int main() {
    char op;
    float num1, num2;

    printf("Enter operator: +, -, *, /: ");
    scanf("%c", &op);

    printf("Enter two operands: ");
    scanf("%f %f", &num1, &num2);

    switch(op) {
        case '+':
            printf("%.1f + %.1f = %.1f\n", num1, num2, num1 + num2);
            break;
        case '-':
            printf("%.1f - %.1f = %.1f\n", num1, num2, num1 - num2);
            break;
        case '*':
            printf("%.1f * %.1f = %.1f\n", num1, num2, num1 * num2);
            break;
        case '/':
            if(num2 != 0)
                printf("%.1f / %.1f = %.1f\n", num1, num2, num1 / num2);
            else
                printf("Error! Division by zero is not allowed.\n");
            break;
        default:
            printf("Error! Invalid operator.\n");
    }

    return 0;
}
