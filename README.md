# SoftGrowTech-_-Invoice-_-Generator

## Project Overview

The **Invoice Generator** is a simple Python application that generates an invoice (bill) based on the items purchased by a customer. The user enters product details such as name, quantity, and price, and the program automatically calculates the total amount and displays a formatted invoice. This project demonstrates **business logic**, **Python programming**, and **basic arithmetic operations**.

# Objectives

* Generate invoices based on customer input.
* Calculate item-wise and total costs.
* Display a professional-looking bill.
* Learn the implementation of business logic in Python.

# Features

* Add multiple products.
* Enter quantity and unit price.
* Automatically calculate subtotal and grand total.
* Display a formatted invoice.
* Menu-driven and easy-to-use interface.

# Technologies Used

* Python 3
* Functions
* Loops
* Lists
* Conditional Statements
* Basic Arithmetic Operations

# File Used

### `invoice_generator.py`

Contains the complete Python program.

# Python Code

```python
def generate_invoice():
    customer = input("Enter Customer Name: ")

    items = []

    while True:
        product = input("Enter Product Name: ")
        quantity = int(input("Enter Quantity: "))
        price = float(input("Enter Price per Unit: "))

        total = quantity * price
        items.append([product, quantity, price, total])

        choice = input("Add another item? (y/n): ").lower()
        if choice != 'y':
            break

    print("\n")
    print("=" * 50)
    print("            INVOICE")
    print("=" * 50)
    print(f"Customer Name: {customer}")
    print("-" * 50)
    print("{:<20}{:<10}{:<10}{:<10}".format("Product", "Qty", "Price", "Total"))

    grand_total = 0

    for item in items:
        print("{:<20}{:<10}{:<10}{:<10}".format(
            item[0], item[1], item[2], item[3]))
        grand_total += item[3]

    print("-" * 50)
    print(f"Grand Total: Rs. {grand_total:.2f}")
    print("=" * 50)


while True:
    print("\n===== INVOICE GENERATOR =====")
    print("1. Generate Invoice")
    print("2. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        generate_invoice()
    elif choice == "2":
        print("Thank you!")
        break
    else:
        print("Invalid choice. Please try again.")
```

# How the Program Works

## Step 1: Start the Program

The following menu appears:

```text
===== INVOICE GENERATOR =====
1. Generate Invoice
2. Exit
```

## Step 2: Enter Customer Information

The program asks for the customer's name.

Example:

```text
Enter Customer Name: Ali
```

## Step 3: Add Products

The user enters:

* Product Name
* Quantity
* Price per Unit

Example:

```text
Enter Product Name: Laptop
Enter Quantity: 2
Enter Price per Unit: 50000
```

The user can continue adding more products.

## Step 4: Generate Invoice

The program calculates each item's total and the overall bill.

Example Output:

```text
==================================================
                INVOICE
==================================================
Customer Name: Ali
--------------------------------------------------
Product             Qty       Price      Total
Laptop              2         50000.0    100000.0
Mouse               1         1500.0     1500.0
--------------------------------------------------
Grand Total: Rs. 101500.00
==================================================
```

## Step 5: Exit

Selecting option **2** closes the application.

```text
Thank you!
```

# Functions Used

### `generate_invoice()`

* Accepts customer details.
* Takes product information.
* Calculates item totals.
* Calculates the grand total.
* Displays the formatted invoice.

# Python Concepts Used

* Variables
* Functions
* Lists
* Loops (`while`, `for`)
* Conditional Statements (`if`, `elif`, `else`)
* User Input (`input()`)
* Arithmetic Operations
* String Formatting (`format()` and f-strings)

# Advantages

* Easy to use.
* Generates accurate invoices automatically.
* Reduces manual calculation errors.
* Demonstrates real-world business logic.
* Beginner-friendly Python project.

# Limitations

* Invoice is not saved to a file.
* No tax or discount calculation.
* No product database.
* No graphical interface.

# Future Enhancements

* Save invoices as text or PDF files.
* Add tax (GST/VAT) calculations.
* Apply discounts.
* Generate invoice numbers automatically.
* Store customer records.
* Create a GUI using Tkinter.
* Export invoices to Excel or PDF.

# Sample Output

```text
===== INVOICE GENERATOR =====
1. Generate Invoice
2. Exit

Enter your choice: 1

Enter Customer Name: Ali

Enter Product Name: Laptop
Enter Quantity: 2
Enter Price per Unit: 50000

Add another item? (y/n): y

Enter Product Name: Mouse
Enter Quantity: 1
Enter Price per Unit: 1500

Add another item? (y/n): n


==================================================
                INVOICE
==================================================
Customer Name: Ali
--------------------------------------------------
Product             Qty       Price      Total
Laptop              2         50000.0    100000.0
Mouse               1         1500.0     1500.0
--------------------------------------------------
Grand Total: Rs. 101500.00
==================================================

===== INVOICE GENERATOR =====
1. Generate Invoice
2. Exit

Enter your choice: 2

Thank you!
```

# Conclusion

The **Invoice Generator** is a simple yet practical Python project that demonstrates the implementation of **business logic** through invoice creation and automatic bill calculation. It helps beginners understand how to use Python for real-world business applications by combining user input, arithmetic operations, loops, functions, and formatted output.
