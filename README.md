# Variables, Functions, and Scope in JS

### Writing functions in JavaScript

1. Write a function named `hiWorld` that prints 'hello world' to the console

```javascript
  function hiWorld(){
    console.log('hello world')
  }
```

2. Write the same function from above in 2 other ways using different syntax

```javascript
  let hiWorld = () => 'hello world'

  let hiWorld = function(){
    console.log('hello world')
  }
```

3. Write a function that accepts a 'name' parameter and prints "Hi, my name is `<name>`" to the console

```javascript
let name = "Swag"
function para(name){
  console.log(`Hi, my name is ${name} `)
}
```

4. Write a funtion that accepts 2 numbers as parameters and returns their sum

```javascript
function sum(a,b){
  return a + b;
}
```

5. Write a function that accepts a number as a parameter returns the double of it

```javascript
function double(num){
  return num * 2
}
```

6. Write a function called `logger` that accepts a string as a parameter and then passes that string to `console.log`. Use `logger` as a callback to console.log each element in the array below. 

```javascript
let stringArray = ["JavaScript", "is pretty", "cool", "I guess."]

// put answer here
function logger(str){
  console.log(str)
} 

stringArray.forEach(function(string){
  logger(string)
})
stringArray.forEach(logger)

for (let i =0; i < stringArray.length; i++){
  logger(stringAray[i])
}
```

7. Write a function that accepts a number as a parameter and prints "❌ You're too young to enter the clurb! ❌" if the parameter 
is less than 21 and "🤡 Welcome to the clurb! 🚀" if the parameter is 21 or over

```javascript
function para(age){
  if (age < 21){
    console.log("❌ You're too young to enter the clurb! ❌")
  } 

  else{
    console.log("🤡 Welcome to the clurb! 🚀")
  }
}
```

8. Modify the above function to allow an underage patron in if they have a fake id

```javascript
function para(age, fakeId = false){
  if (age < 21 && !fakeId ){
    console.log("❌ You're too young to enter the clurb! ❌")
  } 

  else {
    console.log("🤡 Welcome to the clurb! 🚀")
  }
}
```

### Scope in JavaScript

9. What is lexical scope?

```
A lexical scope in JavaScript means that a variable defined outside a function can be accessible inside another function defined after the variable declaration. But the opposite is not true; the variables defined inside a function will not be accessible outside that function.
```

10. What would be printed to the console in the example below? Why?

```javascript
let carType = "Honda Civic"

function myCar(carType){
  console.log(`I drive a fancy ass ${carType}!`)
}

myCar('Tesla X')
```

```
I drive a fancy ass Tesla X!
```

11. What would be printed to the console in the example below? Why?

```javascript
let carType = "Honda Civic"

function myCar(carType){
  console.log(`I drive a fancy ass ${carType}!`)
}

carType('Tesla X')
```

```
```

12. Write out what would be printed to the console, in order, if the script below were run in a browser. 

```javascript

console.log(person) 'nothing'

let person = "Lady Gaga"

function someFunction(){
  console.log(person) 

  function otherFunction(){
    let otherPerson = "Madonna"

    console.log(person)
    console.log(otherPerson)
  }

  otherFunction() "Lady Gaga" "Madonna"

  console.log(person) "Lady Gaga"
  console.log(otherPerson) nothing
}

someFunction() "Lady Gaga"

console.log(otherPerson) nothing
```

```
```

13. What would be printed to the console in the example below? Why?

```javascript
if(true){
  let dogName = "Neikko"
  console.log(`My dog's name is ${dogName}`)
}

console.log(`My dog's name is ${dogName}`)
```

```
"My dog's name is Neikko"
error
```

#### Hoisting

14. In your own words, describe hoisting?
preparation phase and executing phase.


15. If I had a JavaScript file with the following code, what would happen in each of the function calls below? Why?

```javascript
bark()
meow()

function bark(){
  console.log("woof woof")
}

let meow = function(){
  console.log("meeeeooooowwr")
}
```

```
woof woof 
error
```

16. What will the console.log print in each of the examples below? Why?

```javascript
console.log(dogName)

var dogName = "Perky"
```

```javascript
console.log(catName)

const catName = "Houdini"
```

```
error
```

17. What will the console.log print in the example below? Why?

```javascript
horse = "Benny"
console.log(horse)
var horse
```

```
Benny
```

18. With regard to hoisting, what's the difference between `let`, `var`, and `const`

```
let and const doesn't get hoist at preparation phase, var gets hoisted.
```

### Variable declaration

19. What are the differences between declaring variables using `let`, `var`, and `const`?

```
```

### First Class Functions

20. Write a function that accepts a number (e.g. *x*) as a parameter and returns an inner function that accepts a different number (e.g. *y*) as a parameter and returns the product of it and the number from the outer function.

```javascript

function outFunc(x){
  return function(y){
    return x * y
  }
}
```

21. Using the function from above, create a function that accepts a number as a parameter and returns its double. 

```javascript
function outFunc(x){
  return function(y){
    return x * y
  }
}
let doubler = outFunc(2)
doubler(5) //=> 10
```

22. If you successfully got the question above working, explain how you utilized closures to do so?

```
```

23. What would get printed to the console in the example below?

```javascript
let steven = {
  name: "Steven",
  goForRun: function(distance){
    console.log(`Today I ran ${distance} km.`)
  }
}

steven.goForRun // what would happen here?

steven.goForRun()
```

```
```