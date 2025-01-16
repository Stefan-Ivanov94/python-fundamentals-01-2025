# 🖼️ Python Pattern Drawing Project

Welcome to the **Python Pattern Drawing Project**! 🎉 This project is designed to help you understand and implement nested loops, conditional statements, and user inputs in Python.

---

## 📝 Project Overview

Your task is to create various patterns using Python's printing capabilities. You'll build a program where users can choose from different patterns, provide necessary inputs, and see the results displayed in the terminal. 

---

## 🎯 Objectives

- Practice working with **nested loops**.
- Use **if-elif-else conditions** to implement logic.
- Handle **user input** to create dynamic patterns.
- Understand **alignment** using spaces and characters.

---

## 🚀 Patterns to Implement

1️⃣ **Right-angled Triangle**  
```
*
**
***
****
*****
```

2️⃣ **Square with Hollow Center**  
```
*****
*   *
*   *
*   *
*****
```

3️⃣ **Diamond**  
```
  *
 ***
*****
 ***
  *
```

4️⃣ **Left-angled Triangle**  
```
****
***
**
*
```

5️⃣ **Hollow Square**  
```
******
*    *
*    *
*    *
*    *
******
```

6️⃣ **Pyramid**  
```
   *
  ***
 *****
*******
```

7️⃣ **Reverse Pyramid** (New!)  
```
*******
 *****
  ***
   *
```

8️⃣ **Rectangle with Hollow Center** (New!)  
```
********
*      *
*      *
********
```

---

## 📋 Instructions

1️⃣ **Run the Program**  
Start the program and choose a pattern from the menu.  

2️⃣ **Input Dimensions**  
Provide necessary inputs (e.g., number of rows or size of the shape).  

3️⃣ **See the Result**  
Enjoy the output directly in your terminal.  

4️⃣ **Try Again!**  
You can run the program again to explore different patterns.  

---

## 🛠️ Code Skeleton

Below is the **skeleton code** with comments to guide you through the implementation. Your task is to fill in the missing parts and complete the program!

```python
# 🖼️ Python Pattern Drawing Project

# Step 1: Display a menu to the user
print("🌟 Welcome to the Python Pattern Drawing Program!")
print("Choose a pattern type:")
print("1. Right-angled Triangle")
print("2. Square with Hollow Center")
print("3. Diamond")
print("4. Left-angled Triangle")
print("5. Hollow Square")
print("6. Pyramid")
print("7. Reverse Pyramid")
print("8. Rectangle with Hollow Center")

# Step 2: Get the user's choice
choice = int(input("Enter the number corresponding to your choice: "))

# Step 3: Get dimensions based on choice
if choice in [1, 3, 4, 6, 7]:  # Patterns that need the number of rows
    rows = int(input("Enter the number of rows: "))
elif choice in [2, 5, 8]:  # Patterns that need size
    size = int(input("Enter the size of the square/rectangle: "))

# Step 4: Generate the selected pattern
if choice == 1:  # Right-angled Triangle
    for row in range(rows):
        print('*' * (row + 1))

elif choice == 2:  # Square with Hollow Center
    for row in range(size):
        if row == 0 or row == (size - 1):
            print('*' * size)
        else:
            print('*' + (' ' * (size - 2)) + '*')

elif choice == 3:  # Diamond
    for row in range(rows//2 + 1):
        print(' ' * (rows // 2 - row) + '*' * (row * 2 + 1))
    for row in range((rows//2 - 1),-1,-1):
        spacer = ' ' * (rows//2 - row)
        print(spacer + '*' * (2*row +1))

elif choice == 4:  # Left-angled Triangle
    for row in range(rows, 0, -1):
        print('*' * row)

elif choice == 5:  # Hollow Square
    # TODO: Similar to choice 2 but ensure perfect square logic
    pass

elif choice == 6:  # Pyramid
    for row in range(rows):
        spacer = ' ' * (rows - row - 1)
        print(spacer + '*'*(2*row + 1))

elif choice == 7:  # Reverse Pyramid
    for row in range((rows - 1),-1,-1):
        spacer = ' ' * (rows - (row + 1))
        print(spacer + '*' * (2*row + 1))

elif choice == 8:  # Rectangle with Hollow Center
    # TODO: Handle separate width and height inputs for rectangle
    width = int(input("Enter the width of the rectangle: "))
    height = int(input("Enter the height of the rectangle: "))
    for row in range(height):
        if row == 0 or row == height - 1:
            print('*' * width)
        else:
            print('*' + ' ' * (width - 2) + '*')

else:
    print("❌ Invalid choice! Please restart the program.")

# Step 5: Optional - Allow the user to restart or exit
```

---

## 🏁 Conclusion

By completing this project, you'll:
- Master nested loops to create complex patterns. 🌀
- Understand how to manipulate text alignment in Python. 📐
- Get hands-on experience with user inputs and conditional logic. 💻

This is a great stepping stone towards becoming proficient in Python programming. Enjoy your journey and have fun coding! 🚀

---

## 🌟 Bonus Ideas

- Add more patterns like spirals, checkerboards, or alphabets.  
- Enhance the program to allow saving patterns as text files.  
- Add color to the output using libraries like `colorama`.  
