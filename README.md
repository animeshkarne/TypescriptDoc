# TypescriptDoc
# TypeScript Quick Start Guide

## Prerequisites

Before diving into TypeScript, make sure you have a solid understanding of JavaScript basics.

## Getting Started with TypeScript

### Install Node.js and npm

If you don't have Node.js and npm installed, download and install them from [the official website](https://nodejs.org/).

### Install TypeScript

After installing Node.js and npm, open your terminal or command prompt and install TypeScript globally:

```bash
npm install -g typescript
```
## Create a TypeScript Project

Start by creating a new directory for your TypeScript project and navigate into it:
mkdir my-ts-project
cd my-ts-project

## Initialize a TypeScript Configuration File


TypeScript projects typically use a tsconfig.json file to specify compiler options and project settings. You can generate one by running:
tsc --init

## Write TypeScript Code
Create a new TypeScript file with a .ts extension and start writing your TypeScript code. For example, create a file called app.ts and add some code:

```bash
function greet(name: string) {
    console.log(`Hello, ${name}!`);
}
```
greet("TypeScript");

## Compile TypeScript Code
To compile your TypeScript code into JavaScript, run the TypeScript compiler in your project directory:
```bash
tsc
```
This will generate a JavaScript file (app.js) from your TypeScript code.


## Run Your JavaScript Code
You can execute your JavaScript code as you would with any other JavaScript application. For example, you can run it with Node.js:
```bash
node app.js
```
### What is TypeScript?
TypeScript is a superset of JavaScript, which means it includes all JavaScript features and adds some extra features to it. TypeScript is more type-specific, which helps catch errors at compile-time.

Type Annotation in TypeScript
Type annotation is a way of explicitly specifying the type of a variable, function parameter, or function return value. For example:
```bash
const num: number = 10;
const name: string = "Animesh";
const isDone: boolean = true;
```
## Data Types
Number
String
Boolean
Array
Tuple
Enum
Any
Void
Null and Undefined
Object

## Functions in TypeScript
## Optional and Default Parameters

```bash
function greet(name: string, message?: string) {
    if (message) {
        console.log(`${message}, ${name}!`);
    } else {
        console.log(`Hello, ${name}!`);
    }
}

greet("Animesh");
greet("Animesh", "How are you");
```

## Arrays in TypeScript
```bash
const numbers: number[] = [1, 2, 3, 4, 5];
numbers.push(6);
const firstNumber = numbers[0];

Objects in TypeScript

const person: {
  name: string;
  age: number;
  isStudent: boolean;
  address: { city: string; country: string };
} = {
  name: 'Animesh',
  age: 23,
  isStudent: true,
  address: {
    city: 'Shrirampur',
    country: 'India',
  },
};
```

## Type Aliases
```bash
type Person = {
  name: string;
  age: number;
  isStudent: boolean;
  address: { city: string; country: string };
};

const person: Person = {
  name: 'Animesh',
  age: 23,
  isStudent: true,
  address: {
    city: 'Shrirampur',
    country: 'India',
  },
};
```

## Enums in TypeScript
Enums represent a set of named constant values. Example:
```bash
enum Color {
  Red,
  Green,
  Blue,
}

let favoriteColor: Color = Color.Blue;
```

## Tuples in TypeScript
Tuples allow you to store a fixed-size collection of elements of different types. Example:
```bash
type PersonInfo = [string, number, boolean];
const person1: PersonInfo = ['Animesh', 23, true];
const person2: PersonInfo = ['Gaurav', 22, false];
```

## Union and Intersection in TypeScript
Union types allow you to specify that a variable can hold values of multiple types.
```bash
const userInput = (value: number | string) => {
  if (typeof value === 'number') {
    return 'It's a number';
  } else {
    return 'It's a string';
  }
}
```

## Intersection types allow you to combine multiple types into a single type.
```bash
type Person = {
  name: string;
  age: number;
};

type Employee = {
  empId: number;
  department: string;
};

type EmployeeDetails = Person & Employee;
```

## Generics in TypeScript
Generics allow you to create reusable components or functions that can work with multiple data types. Example:
```bash
function logAndReturn<T>(value: T): T {
  return value;
}

const numberResult: number = logAndReturn<number>(100);
const stringResult: string = logAndReturn<string>('Animesh');
const booleanResult: boolean = logAndReturn<boolean>(true);
```

## Generic Multiple Type Variables
```bash
function checkTypes<T,U>(value:T,value2:U):void{
  console.log(typeof value)
  console.log(typeof value2)
}

checkTypes<number,string>(100,'Animesh');
checkTypes<string,number>('Animesh',18);
```

## Interface in Typescript
TypeScript, an interface is a powerful feature that allows you to define a contract for an object's shape. 
It specifies the properties and their types that an object must have to be considered of that particular interface type. 
Interfaces are primarily used for type-checking during development and do not generate any JavaScript code at runtime.
```bash
interface Greet{
  name:string,
  age:number
}

const greet:Greet = {
  name:'Animesh',
  age:23
}
```

## Watch Mode, rootDir, Lib, and More
*watch mode :

just create ts project : tsc --init 
and then :
```bash
tsc --watch
```
for watch mode .

*rootdir and outdir :

inside tsconfig.json file make following changes .
```bash
"rootDir": "./src",
"outDir": "./dist",  
```

*target : for newer update 
```bash
"target": "es2022",
```

### OOPS



