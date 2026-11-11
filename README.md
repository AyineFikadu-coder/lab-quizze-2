
#include <iostream>
using namespace std;
int countPositive(int arr[], int length) {
    int count = 0;

    for (int i = 0; i < length; i++) {
        if (arr[i] > 0) {
            count++;
        }
    }

    return count;
}
int countNegative(int arr[], int length) {
    int count = 0;

    for (int i = 0; i < length; i++) {
        if (arr[i] < 0) {
            count++;
        }
    }

    return count;
    }
int countZero(int arr[], int length) {
    int count = 0;

    for (int i = 0; i < length; i++) {
        if (arr[i] == 0) {
            count++;
        }
    }

    return count;
}
int sumPositive(int arr[], int length) {
    int sum = 0;

    for (int i = 0; i < length; i++) {
        if (arr[i] > 0) {
            sum = sum + arr[i];
        }
    }

    return sum;
}
int sumNegative(int arr[], int length) {
    int sum = 0;

    for (int i = 0; i < length; i++) {
        if (arr[i] < 0) {
            sum = sum + arr[i];
        }
    }

    return sum;
}
double calculateAverage(int arr[], int length) {
    int sum = 0;

    for (int i = 0; i < length; i++) {
        sum = sum + arr[i];
    }

    return (double)sum / length;
}
void displayResults(int positive, int negative, int zero,
                    int positiveSum, int negativeSum,
                    double avg) {

    cout << "\n===== Program Results =====" << endl;
    cout << "Positive numbers: " << positive << endl;
    cout << "Negative numbers: " << negative << endl;
    cout << "Zero values: " << zero << endl;
    cout << "Sum of positive numbers: " << positiveSum << endl;
    cout << "Sum of negative numbers: " << negativeSum << endl;
    cout << "Average of all numbers: " << avg << endl;
}

int main() {
    int numbers[5];

    // Get five integers from the user
    cout << "Enter five integers:" << endl;

    for (int i = 0; i < 5; i++) {
        cout << "Number " << i + 1 << ": ";
        cin >> numbers[i];
    }
    int positive = countPositive(numbers, 5);
    int negative = countNegative(numbers, 5);
    int zero = countZero(numbers, 5);

    int positiveSum = sumPositive(numbers, 5);
    int negativeSum = sumNegative(numbers, 5);

    double avg = calculateAverage(numbers, 5);

    // Display all results
    displayResults(positive, negative, zero,
                   positiveSum, negativeSum, avg);

    return 0;
}

