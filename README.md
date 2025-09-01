# 💱 Currency Converter (C++)

A **simple console program** written in **C++** that converts different currencies into **USD**.  
The program uses a predefined list of exchange rates and demonstrates clean use of **structs, vectors, and functions**.

---

## ✨ Features
- 🌍 Convert supported currencies to **USD**  
- ⚡ Lightweight and fast  
- 🧩 Easy to extend (just add new currency rates)  
- 🧹 Clean and beginner-friendly C++ code  

---

## 🛠 Supported Currencies
| Code | Currency            | Example Rate |
|------|---------------------|--------------|
| USD  | US Dollar           | 1.00 |
| EUR  | Euro                | 0.91 |
| UAH  | Ukrainian Hryvnia   | 42.10 |
| GBP  | British Pound       | 0.77 |
| PLN  | Polish Zloty        | 3.91 |
| JPY  | Japanese Yen        | 146.80 |
| AUD  | Australian Dollar   | 1.54 |
| CAD  | Canadian Dollar     | 1.34 |
| CHF  | Swiss Franc         | 0.86 |
| CNY  | Chinese Yuan        | 7.24 |
| SEK  | Swedish Krona       | 10.52 |
| NOK  | Norwegian Krone     | 10.73 |
| DKK  | Danish Krone        | 6.78 |
| INR  | Indian Rupee        | 83.10 |
| BRL  | Brazilian Real      | 5.05 |
| ZAR  | South African Rand  | 18.60 |
| NZD  | New Zealand Dollar  | 1.68 |
| AED  | UAE Dirham          | 3.67 |

---

## 💻 Code Example
```cpp
double convert_to_usd(double amount, double rate) {
    return amount / rate;
}
Main program:

cpp
Копировать код
cout << "💰 Enter amount: ";
cin >> amount;

cout << "💱 Enter currency code: ";
cin >> from_currency;
▶️ Example Run
yaml
Копировать код
💰 Enter amount: 100
💱 Enter currency code: EUR
💵 100 EUR = 109.89 USD
⚙️ How to Compile & Run
bash

g++ main.cpp -o converter
./converter
🚀 Future Improvements
Add conversion between any two currencies (not just → USD).

Fetch live exchange rates from an API.

Add error handling for lowercase input (eur → EUR).

Build a menu-driven interface for easier usage.
