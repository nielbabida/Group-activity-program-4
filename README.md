# Group-activity-program-4

#include <iostream>
using namespace std;

int main() {
    string name;
    int birthYear, currentYear = 2025, age;

    cout << "Enter your name: ";
    cin >> name;
    cout << "Enter your birth year: ";
    cin >> birthYear;

    age = currentYear - birthYear;

    cout << "\nName: " << name << endl;
    cout << "Age: " << age << endl;

    return 0;
}

#include <iostream>
using namespace std;

int main() {
    int year;
    cout << "Enter a year: ";
    cin >> year;

    if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
        cout << year << " is a leap year." << endl;
    } else {
        cout << year << " is not a leap year." << endl;
    }

    return 0;
}



#include <iostream>
using namespace std;

int main() {
    float num1, num2, num3;

    cout << "Enter three numbers:\n";
    cin >> num1 >> num2 >> num3;

    float largest = num1;
    if (num2 > largest) largest = num2;
    if (num3 > largest) largest = num3;

    cout << "The largest number is: " << largest << endl;

    return 0;
}


#include <iostream>
using namespace std;

int main() {
    double num1, num2;
    char op;

    cout << "Enter two numbers: ";
    cin >> num1 >> num2;
    cout << "Enter operator (+, -, *, /): ";
    cin >> op;

    switch (op) {
        case '+': cout << "Result: " << num1 + num2 << endl; break;
        case '-': cout << "Result: " << num1 - num2 << endl; break;
        case '*': cout << "Result: " << num1 * num2 << endl; break;
        case '/': 
            if (num2 != 0) cout << "Result: " << num1 / num2 << endl;
            else cout << "Error: Division by zero!" << endl;
            break;
        default: cout << "Invalid operator!" << endl;
    }

    return 0;
}


#include <iostream>
using namespace std;

int main() {
    double total = 0, grade;

    cout << "Enter four quarter grades (0-100):\n";
    for (int i = 1; i <= 4; i++) {
        do {
            cout << "Quarter " << i << ": ";
            cin >> grade;

            if (grade < 0 || grade > 100)
                cout << "Invalid grade! Enter a value between 0 and 100.\n";

        } while (grade < 0 || grade > 100);

        total += grade;
    }

    cout << "Average grade: " << total / 4 << endl;

    return 0;
}
