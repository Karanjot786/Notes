# What is Annotations in TypeScript?
In TypeScript, annotations are used to specify the data type of a variable, parameter, function return value, and other types of values.

Annotations are specified using a syntax that involves placing a colon : followed by the data type after the variable name or argument name. For example, the following code declares a variable named name with a type of string:

```ts
let name: string = "Karanjot";
```

# String Annotations

```ts
let message: string = "Hello, world!";
```
# Number Annotations

```ts
let myNumber: number = 42;
```

```ts
let myNumber: number = "Hello, world!"; 
// Error: Type '"Hello, world!"' is not assignable to type 'number'.
```
# Boolean Annotations

```ts
let isCompleted: boolean = false;
```

```ts
let isCompleted: boolean = "not yet"; 
// Error: Type 'string' is not assignable to type 'boolean'.
```

# Type Inference

Type inference is a feature in TypeScript that allows the compiler to automatically determine the type of a variable based on its value.

Here's an example:

```ts
let myString = "Hello, world!";
```

# Any Type

TypeScript has a special any type that can be used to represent any type. When a variable is annotated with the any type, TypeScript will allow it to have any value and disable all type checking for that variable and its properties.

```ts
let myVariable: any = "Hello, world!";
```