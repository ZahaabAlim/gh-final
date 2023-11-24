import sys
def calculate_factorial(number):
   if number < 0:
       return "Factorial is not defined for negative numbers."
   elif number == 0 or number == 1:
       return 1
   else:
       result = 1
       for i in range(2, number + 1):
           result *= i
       return result
# Check if a command-line argument is provided
if len(sys.argv) != 2:
   print("Usage: python script.py <number>")
else:
   # Get the number from the command-line argument
   user_input = int(sys.argv[1])
   # Calculate and print the factorial
   result = calculate_factorial(user_input)
   print(f"The factorial of {user_input} is: {result}")