🧱 clsMyStack - C++ Template-Based Stack Implementation
=====================================================

Overview
--------
`clsMyStack` is a **template-based stack class** in C++ built on top of `clsMyQueue`.  
It provides **Last-In-First-Out (LIFO)** behavior using a doubly linked list internally.  
The class is simple, efficient, and leverages your existing queue implementation. 💻

---

Features
--------
✅ Template-based: works with any data type (int, string, custom objects)  
✅ LIFO stack operations: `push`, `Top`, `Bottom`  
✅ Inherits all queue utilities: `Size`, `IsEmpty`, `Print`, `Reverse`, `UpdateItem`, `Clear`  
✅ Minimal and efficient: reuses `clsMyQueue` functionality  
✅ Easily extendable for custom operations 🔧

---

Class Methods Summary
---------------------
**Stack Operations**
- `push(T Item)` → Pushes an element onto the stack (at the top) ⬆️  
- `Top()` → Returns the element at the top of the stack 🔝  
- `Bottom()` → Returns the element at the bottom of the stack 🔽  

**Inherited Utilities (from clsMyQueue)**
- `pop()` → Removes the top element ✂️  
- `Size()` → Returns the number of elements 🔢  
- `IsEmpty()` → Returns true if stack is empty ⚠️  
- `Print()` → Prints all stack elements from top to bottom 🖨️  
- `Reverse()` → Reverses stack order 🔄  
- `UpdateItem(index, newValue)` → Updates element at a specific index ✏️  
- `Clear()` → Clears the entire stack 🗑️  

---

Example Implementation
----------------------
#include <iostream>
#include "clsMyStack.h"
using namespace std;

int main() {
    clsMyStack<int> stack;

    cout << "Pushing elements 10, 20, 30..." << endl;
    stack.push(10);
    stack.push(20);
    stack.push(30);

    cout << "Stack contents: ";
    stack.Print();

    cout << "Top element: " << stack.Top() << endl;
    cout << "Bottom element: " << stack.Bottom() << endl;

    cout << "Popping top element..." << endl;
    stack.pop();
    stack.Print();

    cout << "Reversing stack..." << endl;
    stack.Reverse();
    stack.Print();

    stack.Clear();
    cout << "Stack cleared. Is empty? " << (stack.IsEmpty() ? "Yes" : "No") << endl;

    return 0;
}

---

Expected Output
---------------
Pushing elements 10, 20, 30...
Stack contents: 30 20 10
Top element: 30
Bottom element: 10
Popping top element...
20 10
Reversing stack...
10 20
Stack cleared. Is empty? Yes ✅

---

Future Extension Ideas
----------------------
1. Add max/min tracking (`TopMax`, `TopMin`) in O(1) 🏆  
2. Add iterator support for range-based loops 🔁  
3. Add `SaveToFile()` / `LoadFromFile()` methods 💾  
4. Implement exception handling for empty stack access ⚠️  
5. Add template specialization for common data types 🧩  
6. Add operator overloading (`+`, `<<`) for stack manipulation ➕  
7. Integrate with smart pointers for memory safety 🛡️  

---

Author & License
----------------
📘 Author: [https://github.com/Faresincode]  
🗓️ Version: 1.0  
📄 License: MIT License  

Open-source, free to use for educational or personal development. 🎓

