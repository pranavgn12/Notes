const student={
	fullName: "Rahul ",
	age: 20,
	cgpa: (String) 8.2
	isPass: true,
};

//objects are key value pairs
//key : value pair

access
student.key
student["key"]


a^b= a**b

=== equal to & type
!== not equal to & type

# data types
Number, String, Boolean, Undefine, Null, Bigit, Symbol
let a; undefined
let var= Null
const sym = Symbol("id");

var : redeclared , global scope.
let : no re declaration but can be updated, block scope.
const: block scope.


for( var of string/array-Var)
for ( i in student) - i gets value of keys in student object.

**Template literal
let obj = {
	item: "pen"
	price: 10,
};

let output = `the cost of ${obj.item} is ${obj.price} rupees`;
console.log(output);

${obj.item} -> place_holder

\t -> escape charcters count as single character

# ARRAYS
array is object
let marks=[22,15,14];
let marks=[22,"aa",true];   Array can have diff data type objects
Array.length
Array is a collection of objects 
object is same too

String is immutable
Array is mutable
for of genrally used in array
for in is also valid

*methods
Array.push(); //adds to end
Array.pop();
Array.toString();
Array.concat(array1,array2);
array.unshift(); //adds to start
array.shift(); //deletes from start and return
array.slice(startidx,endindx) -> returns startidx to endidx-1


array.splice(startidx,delCount,newel1,..)

`Deletes from startidx to delcount then adds new elements from startidx`

splice(2,0,101,102) // inserts elements at idx 2
splice(2) -> deletes and returns from idx 2

# Functions

function Name(){
////////////////
}

# Arrow Functions
const mul = (a,b) => {
	return a*b;
};
mul(a,b);

*higher order function/method : use other function as parameter or returns a function
*callbackfunction is a fn passed as an argument to another function
# Array methods

# forEach()
forEach() is a JavaScript array method that executes a provided function once for each array element. 
It's a convenient way to iterate over an array without using a traditional for loop.

arr.forEach(callbackfun(val,idx,arr));

eg: 
arr = [1,2,3,4,5];
let calsq = (val,idx,arr) => {
    console.log("val^2:",val*val,"",idx,"",arr)
};
arr.forEach(calsq)

# map method
Creates a new array with results from callbackfunction on each element
let newArr = arr.map(callbackfn(val,idx,arr)) 

# filter
newarr= arr.filter(fn); -> accepts elements where fn returns val other than zero

# reduce
arr = [1,2,3,4,5];
const i=0;
const sum = arr.reduce((acc,val) =>{
    return acc+val
}
);
sum = 15



# String methods
toUpperCase()
toLowerCase()
indexOf(searchValue)
lastIndexOf(searchValue)
let text = "JavaScript";
console.log(text.slice(0, 4)); // "Java"
console.log(text.substring(4)); // "Script"
console.log(text.substr(2, 4)); // "vaSc"

let message = "  Hello, world!  ";
console.log(message.trim()); // "Hello, world!"
let original = "I like cats. Cats are cool.";
console.log(original.replace("cats", "dogs")); // "I like dogs. Cats are cool."
console.log(original.replaceAll("cats", "dogs")); // "I like dogs. Dogs are cool."
let str1 = "Hello";
let str2 = "World";
console.log(str1.concat(", ", str2)); // "Hello, World"
let colors = "red,green,blue";
let colorArray = colors.split(",");
console.log(colorArray); // ["red", "green", "blue"]

# DOM
*Writing js as a separate file helps browser caching

**window object** is global object created by browser
window.console.log("hello")
window.alert("meow")

//Object
window -> document where all html & css coild be accesed

console.dir() -> to print objects

console.dir(window.document.body)
then
document.body.style.background="green"
document.body.childNodes[1].innerText="meow"

# DOM Minpulation
once upon a jumped across ocean

document.getElementbyId("")             -># id{} 	in css
document.getElementsByClass("")			-> .class{} in css
document.getElementsByTag("")			

# General 
document.querySelector("# id/.class/tag")   // returns 1st element		
docuemnt.querySelectorALl()                -> returns node list


# DO properties											
innerHTML											
innerText			-> returns the text 	content of element and all its children 							
tagName											
textContent			-> returns content even for hidden elements. ` style="visibility: hidden"							


# Nodes in DOM
text
comment
element

# Attributes
 getAttribute( attr )         <!-- To get attribute value -->
 setAttribute( attr, value)	   ` To set the attribute value 
 
 node.classList
# Class list
 node.classList.add("class_name")
 node.classList.remove("class_name")
 
# Style
 node = document.querySelector()
 node.style   shows inline style
	
*background-color* in css
node.style.*backgroundColor* in js

node.style.color="red"
z
` Inline styles they are

# Insert elements
let el = document.createElement("el");
node.append(el)
node.prepend(el)
node.before(el)
node.after(el)

` note
appendChild() can append only single node
append() can append multiple node and DOMStrings 

removeChild(el)
<!-- The removeChild() method of the Node interface removes a child node from the DOM and returns the removed node. -->

# Delete element
node.remove();

# Events
`Inline`
<button onclick="console.log">
onmousehover

`js
node.event= ()=>
				{
				
				
				}

`if both are defined for same then js is preffered
`if defined twice then newer one overrides 

# Event Object

node.event = (ev)=>{
						console.log(ev.type, ev.target, ev.clientX);
				}
				
# Event Listeners

node.addEventListener( event, callback )
node.removeEventListener( event, callback )

+ Callback refference should be same to remove

+ same event can have multiple fns


# Prototypes in js

__proto__ -> Refference to an object

* prototype is an object inside another object

objects have it.
array is an object.
fns like array.push is in prototype of array

*If both assigned object and prototype has same fn name then object fn is preffered


const p1 = {
  print(){
    console.log("hello")
  }
}

const p2 ={
    print2(){
    console.log("hii2")
  }
}

p2.__proto__ = p1;

` p2.print -> Hello

<!-- if p2 has its own print function then it is used instead of prototype's -->


# Classes and constructor

class myClass{		
	constructor(){}
	myMethod(){}
}
let myObj = new MyClass();
+ new looks and invokes constructor and if constructor is not present it creates constructor

# Inheritence
 class parent{
 }
 
 class child extends parent{
 }
  
* if child and parent have thew same method then child's method will be used
 
 
# Super Keyword
 super(args)					*--> parent constructor*
 super.parentMethod(args)		*--> parent method*
 + super might work only inside class

 *Before using this or returning from child constructor super() should be used.*
 
# Error handling
 
 try{
` ....normal code
 
 } catch(err) {
` ...handling error
 }
 
-------------Example-------------
a= 5;
b=6;
 
console.log(a+b)
console.log(a+b)
console.log(a+b)

console.log(a+c) + C variable doesnt exist abd next statements are not executed

console.log(a+b)
console.log(a+b)
console.log(a+b)
console.log(a+b)
 
+ we can use try and catch to handle the error

a= 5
b=6;
console.log(a+b)
console.log(a+b)
console.log(a+b)


try{
console.log(a+c)
} catch(err){
  console.log(err)
}



console.log(a+b)
console.log(a+b)
console.log(a+b)
console.log(a+b)

# Synchronous


# Asynchronous 

setTimeout(fn,ms)  -> allows program flow and executes fn after certain time


# callback fn
function sum(a,b){
  console.log(a+b);
}

function calculate(a,b,fn){
  fn(a,b);
}

calculate(5,6,sum);




# callbackhell
- Nested callback stacked below one another forming a pyramid structure.

/ex

function getData(dataId,fn){
  setTimeout(()=>{
    console.log("data",dataId);
    if(fn){
    fn();
  }
  }, 2000);
}


getData(1,()=>{
  getData(2,()=>{
    getData(3)
  })
});



# Promises

- A promise can be  Pending, Resolved, Rejected
- Promise is an object
- Promise is a solution to callbackhell

let promise = new Promise(*(resolve, reject)*=>{
.......

`resolve("result") / reject("error");`
})

- P in promise is capital
- function is passed to create promise inside it.
- resolve, reject are 2 handlers which are functions/callbacks.

Promise object can be
* Pending : the result is undefined
* Resolved : the result is a value(fulfilled)
* Rejected : the result is an error object

# Use promises

promise.then((res)=>{})       `when promise is resolved`
promise.catch((err)=>{})      `when promise is rejected`

# promise chaining

ex :
console.log("fetching data 1");
asyncFunc(1).then(()=>{
    console.log("fetching data 2");
    return asyncFunc(2);
}).then(()=>{})


# Async-Await

- async function always returns a promise.
- await pauses the execution of its sorrounding async function until the promise is settled.

      async function myFunc() {

        await getData(1);
        await getData(2);
        ................

      }


# IIFE : Immediately Invoked Function Expression

IIFE is a function that is called immediately as soon as it is defined.

    (fun(){})();


# Fetch API

* Endpoint(url)

let promise = fetch(url, [options])   ----> returns promise

- Uses **Request** **Response** objects.
- The fetch() method is used to fetch a resource(data).

let response = await fetch(url)   ---> returns response object?
status = 200 --> everything ok.

when no *options* are provided by deafualt fetch() calls **GET** Request.

## Terms

  AJAX - Asynchronous JS & XML

  JSON - Javascript Object Notation

  json() - returns a second promise that resolves with the result of parsing the response text as JSON. (Input is JSON, output is JS Object). It is also asychronous method.

  AJAJ - Asynchronous JS & json
  - Most api's today return data in json format so they can be called AJAJ. It is still called AJAX

let data = await response.json();

