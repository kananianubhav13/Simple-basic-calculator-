# Simple-basic-calculator-
def calculator():
    print("=== Simple Calculator ===")
    print("Operations: +  -  *  /")

    while True:
        try:
            # Take inputs
            num1 = float(input("Enter first number: "))
            operator = input("Enter operator (+, -, *, /): ").strip()
            num2 = float(input("Enter second number: "))

            # Perform calculation
            if operator == "+":
                result = num1 + num2
            elif operator == "-":
                result = num1 - num2
            elif operator == "*":
                result = num1 * num2
            elif operator == "/":
                if num2 == 0:
                    print("Error: Cannot divide by zero.")
                    continue
                result = num1 / num2
            else:
                print("Invalid operator! Please use +, -, *, /.")
                continue

            print(f"Result: {result}\n")

        except ValueError:
            print("Invalid input! Please enter numbers only.\n")
        except Exception as e:
            print(f"Unexpected error: {e}")

       
      # Ask if user wants to continue
        choice = input("Do you want to calculate again? (y/n): ").lower()
        if choice != "y":
            print("Exiting calculator. Goodbye!")
            break


# Run calculator
calculator()
