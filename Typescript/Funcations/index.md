# What is Function in TypeScript?

In TypeScript, a function is a block of code that performs a specific task. Functions are the basic building blocks of any application, whether they’re local functions, imported from another module, or methods on a class

## 1. Function Parameter Annotations
## 2. Default Parameters
## 3. Function Return Annotations
## 4. Void In TypeScript
## 5. # Never

# Function Parameter Annotations

Function parameter annotations in TypeScript are used to specify the expected types of the parameters that a function takes.

Here's an example:

```ts
function greet(name: string) {
  console.log(`Hello, ${name}!`);
}
```

```ts
greet(42); 
// Error: Argument of type 'number' is not assignable to parameter of type 'string'.
```

# Default Parameters

Default parameters in TypeScript allow you to specify a default value for a function parameter if one is not provided when the function is called.

Here's an example:

```ts
function greet(name: string = "world") {
  console.log(`Hello, ${name}!`);
}

greet(); // Output: "Hello, world!"
greet("Karanjot Singh"); // Output: "Hello, HuXn!"
```

# Function Return Annotations

Function return type annotations in TypeScript are used to specify the expected return type of a function.

Here's an example:

```ts
function add(a: number, b: number): number {
  return a + b;
}
```

```ts
function add(a: number, b: number): number {
  return "hello";
   // Error: Type 'string' is not assignable to type 'number'.
}
```

# Void In TypeScript

In TypeScript, void is a type that represents the absence of any value. It is often used as the return type for functions that do not return a value.

Here's an example:

```ts
function logMessage(message: string): void {
  console.log(`Message: ${message}`);
}
```


# Never

The never keyword is used to indicate that a function will not return anything, or that a variable can never have a value.

Here are some common use cases for the never type:

1. A function that always throws an error:

```ts
function throwError(msg: string): never {
  throw new Error(msg);
}
```

2. A function that has an infinite loop:

```ts
function infiniteLoop(): never {
  while (true) {}
}
```

3. A variable that can never have a value:

```ts
let x: never;

function neverReturns(): never {
  while (true) {}
}

x = neverReturns();
 // This line will cause a compile-time error because the function never returns
```