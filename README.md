#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    // 사용자로부터 입력 받기
    printf("연산을 선택하세요 (+, -, *, /): ");
    scanf("%c", &operator);
    printf("두 숫자를 입력하세요: ");
    scanf("%lf %lf", &num1, &num2);

    // 연산 수행
    switch (operator) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if (num2 != 0)
                result = num1 / num2;
            else {
                printf("오류: 0으로 나눌 수 없습니다.\n");
                return 1;
            }
            break;
        default:
            printf("오류: 잘못된 연산자입니다.\n");
            return 1;
    }

    // 결과 출력
    printf("결과: %.2lf\n", result);

    return 0;
}
