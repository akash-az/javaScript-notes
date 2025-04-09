# javaScript-notes

#  javaScript-notes

Reference Types : Objects , Arrays , functions > but both Arrays and functions are objects in itself so only reference type is Objects

* Copy by value copy by reference:

// copy by value
* let x = "akash"
* let y = x; // actual value of x is passed to y > value will not change in  
* x = "akashChaturvedi"

 console.log(x); // akashChaturvedi
 console.log(y); // akash

// call by reference

let p = {name : "akash"}
let q = p; // reference of p is passed to q
p.name = "akashChaturvedi"

console.log(p); // {name : "akashChaturvedi"}
console.log(q); // {name : "akashChaturvedi"} > value will change in q too


## Arrays

both size and type are dynamic

const array = ['hello',1,'hye'] 

## hoisting :  accessing value before initializing them. Declaration is called to the top.

## Execution context : environment constituting var, functions scope etc.

Initially global execution context is created > and everytime a function is called a new execution context is created and added to the call stack.

this ec has 2 components(phases) > 
 -> first is actually before running the code i.e memory is allocated to variables and functions and this phase is called memory phase.
 -> 2nd code is executed line by line . JS is a synchronous single threaded language. > one by one single thread executes each code line by line. >  this phase is 
     called code phase.

 * Example : in chrone console when we write

 * createCourse('dsa')
 * console.log(x); // before execution on line 2 this will show undefined bcaus x was 

 *  before even executing this code if we put a break point in snippet section on line2 , the console will show undefined , but the code wasn't even executed.

##  window
every time our code runs a global object is created , in browser it is called window in node js it is something else.

Example : 
  console.log(a); // undefined
  var a = 10;
  console.log(a); // 10
  console.log(this.a); // 10 > this here referes to the global object a
  console.log(window.a); // 10 > window also referes to the global object a.
       

 







