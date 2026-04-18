#include <iostream>
using namespace std;

int main() {

    float expense;
    float total = 0;
    float foodTotal = 0;
    float travelTotal = 0;
    float shoppingTotal = 0;

    int mainChoice;
    int category;

    do {
        cout << "\n===== Expense Tracker =====\n";
        cout << "1. Add Expense\n";
        cout << "2. View Summary\n";
        cout << "3. Exit\n";
        cout << "Enter your choice: ";
        cin >> mainChoice;

        if (mainChoice == 1) {

            cout << "\nSelect Category:\n";
            cout << "1. Food\n";
            cout << "2. Travel\n";
            cout << "3. Shopping\n";
            cout << "Enter category number: ";
            cin >> category;

            cout << "Enter expense amount: ";
            cin >> expense;

            total += expense;

            if (category == 1)
                foodTotal += expense;
            else if (category == 2)
                travelTotal += expense;
            else if (category == 3)
                shoppingTotal += expense;
            else
                cout << "Invalid Category!\n";
        }

        else if (mainChoice == 2) {

            cout << "\n----- Expense Summary -----\n";
            cout << "Food Total: " << foodTotal << endl;
            cout << "Travel Total: " << travelTotal << endl;
            cout << "Shopping Total: " << shoppingTotal << endl;
            cout << "Overall Total: " << total << endl;
        }

        else if (mainChoice == 3) {
            cout << "Exiting Program...\n";
        }

        else {
            cout << "Invalid Choice!\n";
        }

    } while (mainChoice != 3);

    return 0;
}
