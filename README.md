# Working-of-javascript-assignment

Ques 1  Write a function called "addnumber" that take two Number a argument and return their sum. Call all the function Before it is declared to demonstrate  hosting 

Ans  In JavaScript, function declarations are hoisted, meaning they can be called before they are declared in the code. Here's an example of a function called "addNumbers" that takes two numbers as arguments and returns their sum, demonstrating function hoisting:

// Call the function before it's declared
const result = addNumbers(5, 3);
console.log("Result before function declaration:", result);

// Function declaration (hoisted)
function addNumbers(a, b) {
  return a + b;
}

// Call the function after it's declared
const sum = addNumbers(10, 20);
console.log("Result after function declaration:", sum);


In this code:

We first call the addNumbers function before it's declared, and then we call it after the declaration.

The function is declared afterward, and it is still called successfully, demonstrating function hoisting.

When you run this code, you will see that the function can be called both before and after its declaration because function declarations are hoisted to the top of the scope in which they are defined


Ques 2   Write a function called "multiplyNumbers" that takes two Numbers as arguments and returns their product. Use function expressions to define the function and call the function Before it is declared to demonstrate hosting 

Ans   In JavaScript, function expressions are not hoisted like function declarations. When you use a function expression, you cannot call the function before it's declared. However, I can show you an example of defining a function expression and then calling it:

// Function expression (not hoisted)
const multiplyNumbers = function(a, b) {
  return a * b;
};

// Call the function after it's declared
const product = multiplyNumbers(5, 3);
console.log("Result after function declaration:", product);


In this code:

We define a function expression multiplyNumbers using the const keyword.

Unlike function declarations, function expressions are not hoisted, so we cannot call the function before it's declared.

We call the multiplyNumbers function after it's declared.

This demonstrates the behavior of function expressions, which need to be defined before they can be called.


Ques  3  Write a function that takes two Numbers as arguments and returns their sum. Declare a Variable inside the function using the var keyword and log its value to the console Before it is assigned a value to demonstrate Variable hosting 

Ans  In JavaScript, variables declared using the var keyword are hoisted to the top of their containing function or global scope, which means they are initialized with the value undefined. Here's an example to demonstrate variable hoisting using a var declaration:

function addNumbers(a, b) {
  // Declare a variable using var (hoisted with value undefined)
  var result;
  
  // Log the value of 'result' before it's assigned
  console.log("Result before assignment:", result);
  
  // Assign a value to 'result'
  result = a + b;
  
  // Return the result
  return result;
}

const sum = addNumbers(5, 3);
console.log("Sum:", sum);


In this code:

We declare a variable named result inside the addNumbers function using the var keyword. This variable is hoisted to the top of the function and initialized with the value undefined.

We log the value of result before it's assigned a value. This demonstrates that, when hoisted, var variables are available but have an initial value of undefined.

After logging the initial value, we assign a value to result, which is the sum of the two input numbers.

Finally, we return and log the result of the addition.

When you run this code, you'll see that the value of result is undefined when logged before assignment, demonstrating variable hoisting. After assignment, it holds the sum of the input numbers.

Ques  4   Declare three variables one using let, one using var, and one using const, all inside a block scope. Assign them values and log their values to the console Before and after they are declared to demonstrate Variable  hosting 

In JavaScript, variable declarations using let and const are block-scoped, which means they are only accessible within the block where they are defined. Variables declared with var have a function or global scope. Here's an example that demonstrates variable hoisting with all three variable types:

// Block scope
{
  // Declare variables inside a block
  let variableLet;
  var variableVar;
  const variableConst = 42;

  // Log the values before they are assigned
  console.log("Before assignment (let):", variableLet);
  console.log("Before assignment (var):", variableVar);
  console.log("Before assignment (const):", variableConst);

  // Assign values to the variables
  variableLet = "I'm a let variable";
  variableVar = "I'm a var variable";

  // Variables declared with 'const' must be assigned when declared
}

// Log the values after assignment
console.log("After assignment (let):", variableLet);
console.log("After assignment (var):", variableVar);
console.log("After assignment (const):", variableConst);

In this code:

Inside a block, we declare three variables: variableLet using let, variableVar using var, and variableConst using const.

We log the values of these variables before they are assigned. Because they are all hoisted to the top of the block, they have an initial value of undefined.

We assign values to variableLet and variableVar.

Variables declared with const must be assigned when declared, so they have no initial "uninitialized" value. We didn't log their values before assignment.

Finally, we log the values of these variables after assignment.

When you run this code, you'll observe that the values of variableLet and variableVar are undefined before assignment and have their assigned values after assignment. variableConst is not accessible before assignment because it must be assigned when declared, and it retains its assigned value after assignment.

Ques 5  Declare a Variable using let inside a Block scope and attempt to log its value to the console Before it is Assigned a value to demonstrate the temporal dead zone.

Ans   {
  // Declare a variable inside a block
  let variableLet;
  
  // Attempt to log its value before assignment
  console.log("Before assignment (let):", variableLet); // This line will throw a ReferenceError
  
  // Assign a value to the variable
  variableLet = "I have a value now!";
  
  // Log its value after assignment
  console.log("After assignment (let):", variableLet);
}

In this code:

Inside a block, we declare a variable variableLet using let.

We attempt to log the value of variableLet before it is assigned a value. This will throw a ReferenceError because the variable is in the Temporal Dead Zone.

After the variable is assigned a value, we log its value.

When you run this code, you'll see that the attempt to log the value of variableLet before assignment results in a ReferenceError, demonstrating the concept of the Temporal Dead Zone. Once a value is assigned to the variable, it can be accessed and logged without any issues.




