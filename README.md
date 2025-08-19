# Pointer_Operations_In_CPP
# Aim
To study and implement pointer operations (call by refernce and call by value) in C++.

# Tools
Visual Studio Code
# Theory
## Call by Value:
Mechanism: When an argument is passed by value, a copy of the actual argument's value is made and passed to the function's formal parameter. Effect on Original Data: Any modifications made to the formal parameter within the function do not affect the original variable in the calling scope, as the function operates on a separate copy. Syntax: Standard parameter declaration (e.g., void func(int x)).

## Call by Reference:
Mechanism: When an argument is passed by reference, the address (or a reference/alias) of the actual argument is passed to the function's formal parameter. This means the formal parameter directly refers to the same memory location as the original variable. Effect on Original Data: Modifications made to the formal parameter within the function do affect the original variable in the calling scope, as both refer to the same data. Syntax: Using the reference operator (&) in the parameter declaration (e.g., void func(int& x)). Alternatively, passing a pointer to the variable allows for similar behavior, where the pointer holds the address of the original variable

# Comparison: Call by Value vs Call by Reference

| Aspect | Call by Value | Call by Reference |
|--------|---------------|-------------------|
| **Mechanism** | A copy of the variable is passed to the function | The reference (alias) or address of the variable is passed |
| **Effect on Original Data** | Changes inside the function do not affect the original variable | Changes inside the function directly affect the original variable |
| **Memory Usage** | Requires extra memory to store copies | More memory efficient as no copies are created |
| **Performance** | Slower for large data structures due to copying | Faster for large data structures since only a reference is passed |
| **Safety** | Safer, as the original data is protected | Less safe, as the original data may be unintentionally modified |
| **Syntax** | `void func(int x)` | `void func(int &x)` or `void func(int *x)` |
| **Use Case** | Suitable when the original value should remain unchanged | Suitable when the function must modify the original value or handle large data efficiently |
# Algorithms

## 1. Swapping Numbers using Call by Value
1. Start  
2. Input two numbers `a` and `b`  
3. Call `swap(x, y)` (values passed)  
4. Swap occurs inside the function but does not affect the original variables  
5. Print values (remain unchanged)  
6. End  

---

## 2. Swapping Numbers using Call by Reference
1. Start  
2. Input two numbers `a` and `b`  
3. Use a function `swap(&x, &y)` with references  
4. Store `x` in `temp`  
5. Assign `y` to `x`  
6. Assign `temp` to `y`  
7. Print swapped values (original variables get swapped)  
8. End  

---

## 3. Reversing a String
1. Start  
2. Input a string  
3. Count its length  
4. Swap characters from start and end, moving towards the center  
5. Print the reversed string  
6. End  

---

## 4. Salary Hike
1. Start  
2. Input: years completed, research projects, new research projects, company profit  
3. Initialize `conditions_met = 0`  
4. Check each condition:  
   - If years > 1 → increment `conditions_met`  
   - If research projects ≥ 1 → increment `conditions_met`  
   - If new projects ≥ 1 → increment `conditions_met`  
   - If profit > 100000 → increment `conditions_met`  
5. If `conditions_met ≥ 3`:  
   5.1 Input current salary  
   5.2 Increase it by 20% (using bonus function)  
   5.3 Print new salary  
6. Else: Print `"Not eligible for salary hike"`  
7. End  
# Conclusion
We learnt to use pointers in different types of operations . We learnt about 'call by refernce ' and 'call by value' methods
