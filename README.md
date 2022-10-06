# Day_10-Calculator
using concept of python
- functions
- whlie loop
- recursion

```
from art import logo


#addition
def add(n1, n2):
  return n1+n2

#subtraction
def subtract(n1, n2):
  return n1-n2

#multiply
def multiply(n1, n2):
  return n1*n2

#divide
def divide(n1, n2):
  return n1/n2

def calculator():
  print(logo)
  n1=float(input("enter the fist number: "))
  operations={"+": add,
              "-": subtract,
              "*": multiply,
              "/": divide}
  
  for symbol in operations:
    print(symbol)
  continue_calulation=True
  while continue_calulation==True:
  
    operation_symbol=input("Pick an operation: ")
    n2 = float(input("enter the next number: "))
    calculation_function = operations[operation_symbol]
    answer = calculation_function(n1, n2)
    print(f"{n1} {operation_symbol} {n2} = {answer}")
    
    if input(f"Type 'y' to continue calculating with {answer}, or type 'n' to start new calculation. ") == "y":
      n1=answer
    else:
      continue_calulation=False
      calculator()
### Recursion      
calculator()     
```
