# My String Library (ClsString)

An elegant, object-oriented C++ library designed to extend and simplify standard string manipulation. Built from scratch as a practical implementation of Object-Oriented Programming (OOP) concepts, this library provides a robust set of static and non-static methods for text parsing, formatting, and analysis.

---

## ✨ Features

The library is divided into logical utility categories:

### 1. Case Manipulation
* Convert entire strings to UPPERCASE or lowercase.
* Capitalize or decapitalize the first letter of every word.
* Invert the case of all characters in a string.

### 2. Counting & Analysis
* Count total words in a string.
* Count capital or small letters.
* Count specific characters (with case-sensitivity toggle).
* Count and print vowel letters (`a, e, i, o, u`).

### 3. Trimming & Cleaning
* Trim spaces from the Left, Right, or Both sides of a string.
* Remove all punctuation marks from the text.

### 4. Splitting, Joining & Reversing
* Split strings into a vector of strings based on custom delimiters.
* Join vector elements back into a single string.
* Reverse word order in a sentence.
* Replace words or substrings dynamically.

---

## 🚀 Usage Examples

The class supports both **Static** (stateless) and **Object-Oriented** (stateful) approaches.

```cpp
#include <iostream>
#include "ClsString.h"

using namespace std;

int main() {
    // --- 1. Object-Oriented Approach ---
    ClsString str("   hello custom string library!   ");

    // Using Properties (Get / Set)
    cout << "Original: " << str.Value << endl;

    // Trimming and Capitalizing
    str.Value = str.Trim();
    cout << "Trimmed: " << str.Value << endl;
    cout << "Capitalized: " << str.MakeFirstLetterCaptalOfString() << endl;

    // --- 2. Static Method Approach ---
    string text = "C++#//#OOP#//#Library";
    vector<string> words = ClsString::SplitString(text, "#//#");

    cout << "\nSplit words using static method:" << endl;
    for (const string& word : words) {
        
        cout << "- " << word << endl;
    }

    return 0;
}
