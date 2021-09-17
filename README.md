# Sprint Challenge - JavaScript Fundamentals

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in project. This Sprint explored JavaScript Fundamentals. During this Sprint, you studied array methods, this keyword, prototypes, and class syntax. In your challenge this week, you will demonstrate proficiency by completing a range of JavaScript problems.

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the sprint challenge. 

## Introduction

The index.js file contains all of your challenges. Please review it in full before answering the questions. If you complete the stretch goals please leave them in your file but commented out so that they do not affect the MVP tasks 

In meeting the minimum viable product (MVP) specifications listed below, you should have all tests passing. You can console.log to check your work and ensure you are submitting the correct results 

### Commits

Set up codegrade early and commit your code regularly and meaningfully. 

## Interview Questions
### (please edit this file and write your answer below each question.)
Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read.

1. Explain the differences between `.map`, `.reduce` and `.filter` and describe a use case for each. 
MAP - 
    The map array method returns an array based on the original array but doesn't mutate the original array; it also allows you to modify the original array based on whatever you want. An example of this would be recieving an array of objects [{firstName: 'John'}, {firstName: 'Mark'}] then mapping over that array to add a new property on each of those objects like this:
       const arrWithWorkersProp =  [{firstName: 'John'}, {firstName: 'Mark'}].map(obj => {
           obj.employed = true; 
           return obj
       });

REDUCE - 
    The reduce method returns a value from looping over an array like object. The value returned can be many things, an object, and array, a number, a string, etc. A common use case would be to get the sum of arrays within a number like this:
        const sum = [1, 2, 3, 4, 5].reduce((acc, cur) => acc + cur;, 0) // 17
FILTER - 
    The filter array method returns an array based on the original array according to a condition by which you want each array element to satisfy. A use case for this would be checking whether or not objects within an array satisfy a condition. Like this:
        const newArr = [{firstName: 'John'}, {firstName: 'Mark'}].filter(nameObj => nameObj.firstName === "John" && nameObj);
        console.log(newArr); // this will return [{firstName: 'John'}]. Then we could do what we want with this new array.

2. Explain the difference between a callback and a higher order function.
    A callback function is a function that is passed into another function as an parameter; to be invoked. Like so:
        const callBack = function(){return `I'm a callback function`}
        const higherOrderFunction(callBack){callBack();} // this will return `I'm a callback function;
    A higher order function is a function that recieves functions as parameters as demonstrated above. A higher order function can also be a function what returns another function like below:
        function higherOrderFunctionByReturn(){ return function(){console.log(`Im being returned by a higher order function`)}}
3. Explain what a closure is.
    A closure is when an nested function reaches into it's parent scope to define a variable not defined within its own scope.
4. Describe the four principles of the 'this' keyword.
    1. When the this keyword is used without context, like in a function contained in the global scope, this this keyword refers to the window object.
    2. When a function is called with a dot to the left, the this keyword within that function will refer to the object to the left of that dot.
    3. When used within a contructor function, the this keyword refers to the specific instance of that object returned by the contructor function.
    4. When using call, bind, or apply; the this keyword within that function is defined by whatever you place into those methods first parameter.
5. Why do we need super() in an extended class?
    The super(args) is syntactic sugar for Parent.call(this, args). The super allows the extended class to inherit the properties from the parent class.
You are expected to be able to answer questions in these areas. Your responses contribute to your Sprint Challenge grade. 

## Instructions

### Task 1: Set up Project

Using VSCode and Command Line:


1. Fork the repo
2. Clone your forked version of the repo
<!-- I created a new branch with my name and pushed it to my repo. Didn't show up on codegrade, so I merged with master then pushed and it showed up on codegrade. -->
3. cd into your repo and create a branch with your first and last name
4. open the terminal in your vs code and type `npm install`
5. next type `npm run test` in your terminal
6. Complete your work making regular commits, once you have all your tests passing and you are ready to submit your work please see canvas for instructions on how to submit

### Testing & Debugging

Open a second terminal inside of your project by clicking on the split terminal icon
![alt text](assets/split_terminal.png "Split Terminal")

Inside of your second terminal type `npm start` 
![alt text](assets/npm_start.png "type npm start")

You will be running your tests in one terminal and debugging in the other. As you work on your code you should make use of `console.log` to check your progress and debug.
![alt text](assets/tests_debug_terminal_final.png "your terminal should look like this")

### Task 2: Project Requirements (MVP)

You must complete all tasks inside of `index.js` and answer the questions above.

In your solutions, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Resources
 
 [Sprint Challenge Study Guide](https://www.notion.so/lambdaschool/Unit-1-Sprint-3-Study-Guide-033a9a00659a4ef98c12eb97e49a6110)

## Submission format

Please submit your project via codegrade by following [these instructions](https://www.notion.so/lambdaschool/Submitting-an-assignment-via-Code-Grade-A-Step-by-Step-Walkthrough-07bd65f5f8364e709ecb5064735ce374)

