#include <iostream>
#include <vector>

int main() {
    // Введіть розмір масиву A (2N)
    int N;
    std::cout << "Введіть N: ";
    std::cin >> N;

    // Ініціалізуємо масив A
    std::vector<int> A(2 * N);
    std::cout << "Введіть " << 2 * N << " елементів масиву A:\n";
    for (int i = 0; i < 2 * N; i++) {
        std::cin >> A[i];
    }

    // Створюємо масив B розміру 2N
    std::vector<int> B(2 * N);

    // Копіюємо другу половину масиву A в першу половину масиву B
    for (int i = 0; i < N; i++) {
        B[i] = A[N + i];
    }

    // Копіюємо першу половину масиву A в другу половину масиву B
    for (int i = N; i < 2 * N; i++) {
        B[i] = A[i - N];
    }

    // Виводимо масив B
    std::cout << "Масив B після операції:\n";
    for (int i = 0; i < 2 * N; i++) {
        std::cout << B[i] << " ";
    }
    std::cout << std::endl;

    return 0;
}
