# Number-of-X-s

#include <iostream>

using namespace std;

int countOccurrences(int number, int digit) {
    int count = 0;
    while (number > 0) {
        if (number % 10 == digit) {
            count++;
        }
        number /= 10;
    }
    return count;
}

int main() {
    int L, R, X;
    cin >> L >> R >> X;

    int totalOccurrences = 0;

    for (int num = L + 1; num < R; ++num) {
        totalOccurrences += countOccurrences(num, X);
    }

    cout << totalOccurrences << endl;

    return 0;
}
