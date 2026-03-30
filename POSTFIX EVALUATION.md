# Exp.No:33  
## POSTFIX EVALUATION

---

### AIM  
To write a Python program to evaluate a user-given Postfix expression that contains Multiplication and Addition operators using the stack concept.

---

### ALGORITHM

1. **Start the program.**
2. Define a set named `OPERATORS` containing all the valid operators: `*, +, **, -, /, %`.
3. Define a function `evaluate_postfix(exp)` to evaluate the postfix expression:
   - Inside the function, create an empty list called `stack` to store operands and intermediate results.
4. Loop through each item in the given postfix expression:
   - If the current item is **not in OPERATORS**, it is an operand, so append it to the stack.
   - If the current item is an **operator**:
     - Pop the top two elements from the stack (first pop is `a`, second pop is `b`).
     - Perform the operation `b <operator> a` depending on the current operator.
     - Store the result in a variable called `result`.
     - Append the result back to the stack.
5. After the loop ends, return the first element of the stack as the final evaluation result.
6. Take a postfix expression as input from the user.
7. Print the postfix expression.
8. Call the function `evaluate_postfix()` with the input and print the result.
9. **End the program.**

---

### PROGRAM

```
OPERATORS=set(['*','+']) 
def evaluate_postfix(expression):
    stack=[]
    for i in expression:
        if i not in OPERATORS:
            stack.append(i)
        else:
            a=stack.pop()
            b=stack.pop()
            if i=='*':
                r=int(b)*int(a)
            elif i=='+':
                r=int(b)+int(a)
            stack.append(r)
    return stack[0]
expression = input()
print("postfix expression: ",expression)
print("Evaluation result: ",evaluate_postfix(expression))
```

### OUTPUT
<img width="1181" height="212" alt="515163574-d553f1f8-e86e-4a1b-aa92-ac970f5d6635" src="https://github.com/user-attachments/assets/10f6f4fb-7875-49ae-b73f-bed22355facd" />


### RESULT

Therefore, the output is the example to write a Python program to evaluate a user-given Postfix expression that contains Multiplication and Addition operators using the stack concept.
