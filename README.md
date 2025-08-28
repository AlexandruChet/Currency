# 💱 Currency Converter

A simple **C++ program** to convert various currencies to **USD**.

---

## 🔹 Features

- Convert any supported currency to USD
- Easy to extend with new currencies
- Simple and clean code

---

## 💻 Code

```cpp
#include <iostream>
#include <vector>
#include <iomanip>
#include <string>
using namespace std;

struct Item {
    string text;
    double rate;
};

double convert_to_usd(double amount, double rate) {
    return amount / rate;
}

int main() {
    vector<Item> items = {
        {"USD", 1}, {"EUR", 0.91}, {"UAH", 42.1}, {"GBP", 0.77},
        {"PLN", 3.91}, {"JPY", 146.8}, {"AUD", 1.54}, {"CAD", 1.34},
        {"CHF", 0.86}, {"CNY", 7.24}, {"SEK", 10.52}, {"NOK", 10.73},
        {"DKK", 6.78}, {"INR", 83.1}, {"BRL", 5.05}, {"ZAR", 18.6},
        {"NZD", 1.68}, {"AED", 3.67}
    };

    double amount;
    string from_currency;

    cout << "Enter amount: ";
    cin >> amount;

    cout << "Enter currency: ";
    cin >> from_currency;

    double from_rate = 0;
    for (const auto &i : items) {
        if (i.text == from_currency) {
            from_rate = i.rate;
            break;
        }
    }

    if (from_rate == 0) {
        cout << "Error: Currency not found!" << endl;
        return 1;
    }

    double result = convert_to_usd(amount, from_rate);
    cout << fixed << setprecision(2);
    cout << amount << " " << from_currency << " = " << result << " USD" << endl;

    return 0;
}
