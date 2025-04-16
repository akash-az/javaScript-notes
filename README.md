# javaScript-notes


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

## hoisting :  accessing value before initializing them. Declaration is called to the top. let,var,const are all hoisted but only var is assigned undefined and other two is assigned nothing.
## Temporal Dead Zone : let,const values are hoisted but they are not accessible.they are in temporal dead zone which why accessing it gives reference error.
   *  With let (and const), hoisting still happens, but the variable is in a "temporal dead zone" from the start of the block until the declaration is encountered.
   * in other words bcus var is initialized with undefined v
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
  * if console.log(window); // window object will be shown on the console which will contain variable a = 10.
  * if (window === this ) // will return true.

## let ,const , var

 var is created in global scope.
 let, const is created in scripts which is a different space. 
  example : declare var a = .. , lt , const .. in chrome snippet
            ctrl + enter > in scope in global a will be present but in scripts  let and const variables will be present.

            
## lexical scope :  

 function printmsg(){
 console.log(x);  // first x will be searched in local/lexical scope ,if not found then it will be searched in global scope.
 }

 let x = 5;
 printmsg();

 ## function / aka First class citizens > can assigned to other variables , different data structures and passed or returned from another function.

1>

function sum (a,b){
 return a + b;  // this function here in its local , not only has values of a and b but has " this : window " , which is a reference to global scope.
  } 

 console.log(sum); // prints the entire function body as is on the console
 console.log(sum(5,6)); // prints the sum of the function

2>

let sum =  function (a,b){
 return a + b;
 } 

 console.log(sum); // prints the entire function body as is on the console
 console.log(sum(5,6)); // prints the sum of the function

 3> passing function as a parametre

  let a = function (x,y)
  {
  return x+y;
  }

  let b = function (x,y) { return x - y; }

  function operate (operations, x,y){ return operations(x,y); } // function passed as a parametre. 

  console.log(operate(a,5,6));
  console.log(operate(b,7,8));


 ## closures : function with its lexical scope(which has reference to outer variables) is called closure
     using too much closure results in memory leaks.


 ## Async Js 

 * Callbacks : 


## fetch :

response = fetch(" api ");

Now 2 things happen : 1 >  memory is created for data , and two arrays onFulfilled, onRejection are made which are inaccessible to users. 

2> this part handles the browser/node request. A network request is fired and this request requires resources which is provided by either browser/node. On succession/failure of network response,respective function is executed either in onFullfilled  or onRejection based on promise fullfillment.And then these function resolves data variable which is stored in the the response.

 
 
 
            
  

    
    
  
       

 







