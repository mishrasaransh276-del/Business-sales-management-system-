[Business_Sales_Management_System_Internship_Project.pdf](https://github.com/user-attachments/files/24339899/Business_Sales_Management_System_Internship_Project.pdf)
[Business_Sales_Management_System_Internship_Project.pdf](https://github.com/user-attachments/files/24339875/Business_Sales_Management_System_Internship_Project.pdf)
[Business_Sales_Management_System_Internship_Project.pdf](https://github.com/user-attachments/files/24339860/Business_Sales_Management_System_Internship_Project.pdf)
# Business-sales-management-system-
A python based business sales management system developed as a 15 day internship project 
# ==================================================
# Business Sales Management System
# 15 Days Internship Project
# Developed by: Saransh Mishra
# ==================================================

# Product list with prices
products = {
    "Laptop": 50000,
    "Mobile": 20000,
    "Headphones": 2000,![WhatsApp Image 2025-10-10 at 09 54 19_5b78690e](https://github.com/user-attachments/assets/63aae8f4-cb5b-4fe9-96d0-90a1cdb14e8a)

    "Keyboard": 1500,
    "Mouse": 800
}

# Dictionary to store sales data
sales = {}

# Function to display available products
def show_products():
    print("\nAvailable Products:")
    print("-------------------")
    for product, price in products.items():
        print(f"{product} : ₹{price}")

# Function to sell a product
def sell_product():
    product = input("\nEnter product name: ").title()
    if product in products:
        try:
            quantity = int(input("Enter quantity: "))
            total_price = products[product] * quantity
            sales[product] = sales.get(product, 0) + total_price
            print(f"✅ Sale Successful! Total Amount: ₹{total_price}")
        except ValueError:
            print("❌ Please enter a valid quantity.")
    else:
        print("❌ Product not available.")

# Function to generate sales report
def sales_report():
    print("\nSales Report")
    print("------------")
    if not sales:
        print("No sales recorded yet.")
        return

    total_revenue = 0
    for product, amount in sales.items():
        print(f"{product} : ₹{amount}")
        total_revenue += amount

    print("-------------------")
    print(f"Total Revenue: ₹{total_revenue}")

# Main menu
def main_menu():
    while True:
        print("\n====== Business Sales Management System ======")[Business_Sales_Management_System_Internship_Project.pdf](https://github.com/user-attachments/files/24338783/Business_Sales_Management_System_Internship_Project.pdf)
[sales_management.py](https://github.com/user-attachments/files/24338782/sales_management.py)
[Business_Sales_Management_System_Internship_Project.pdf](https://github.com/user-attachments/files/24338781/Business_Sales_Management_System_Internship_Project.pdf)

        print("1. Show Products")
        print("2. Sell Product")
        print("3. Sales Report")
        print("4. Exit")

        choice = input("Enter your choice (1-4): ")

        if choice == "1":
            show_products()
        elif choice == "2":
            sell_product()
        elif choice == "3":
            sales_report()
        elif choice == "4":
            print("\nThank you for using the system!")
            break
        else:
            print("❌ Invalid choice. Please try again.")

# Run the program
if __name__ == "__main__":
    main_menu()
