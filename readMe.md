# A Short JS and Node.js tutorial



### JavaScript Variables

```javascript
const name = "Ali";
let money;
money = 2000.50;
```

### Variable Scope

```javascript
const myVar = 'global'; // Declare a global variable
function checkscope( ) {
  const myVar = 'local'; // Declare a local variable
  console.log(myVar);
}
```

### Operator and Description

- +(Addition)
  - Adds two operands Ex: A + B will give 30
- -(Subtraction)
  - Subtracts the second operand from the first Ex: A - B will give -10
- *(Multiplication)
  - Multiply both operands Ex: A * B will give 200
- / (Division)
  - Divide the numerator by the denominator Ex: B / A will give 2
- % (Modulus) Outputs the remainder of an integer division Ex: B % A will give 0
- ++ (Increment)
  - Increases an integer value by one Ex: A++ will give 11
- -- (Decrement)
  - Decreases an integer value by one Ex: A-- will give 9

### Logical Operators

- && (Logical AND)
  - If both the operands are non-zero, then the condition becomes true. Ex: (A && B) is true.
- || (Logical OR)
  - If any of the two operands are non-zero, then the condition becomes true. Ex: (A || B) is true.
- ! (Logical NOT)
  - Reverses the logical state of its operand. If a condition is true, then the Logical NOT operator will make it
- false. Ex: ! (A && B)
  - is false. Assignment Operators

### Operator and Description

- = (Simple Assignment )
  - Assigns values from the right side operand to the left side operand
    Ex: C = A + B will assign the value of A + B into C
- += (Add and Assignment)
  - It adds the right operand to the left operand and assigns the result to the left operand.
    Ex: C += A is equivalent to C = C + A
- −= (Subtract and Assignment)
  - It subtracts the right operand from the left operand and assigns the result to the left operand.
    Ex: C -= A is equivalent to C = C - A
- *= (Multiply and Assignment)
  - It multiplies the right operand with the left operand and assigns the result to the left operand.
    Ex: C *= A is equivalent to C = C * A
- /= (Divide and Assignment)
  - It divides the left operand with the right operand and assigns the result to the left operand.
    Ex: C /= A is equivalent to C = C / A
- %= (Modules and Assignment)
  - It takes modulus using two operands and assigns the result to the left operand.
    Ex: C %= A is equivalent to C = C % A

### if...else statement

```javascript
const age = 15;

if ( age > 18 ) {
  console.log('Qualifies for driving');
} else {
  console.log('Does not qualify for driving');
}

```

### For Loop

```javascript
let count;
console.log('Starting Loop');

for (count = 0; count < 10; count++) {
  console.log('Current Count : ' + count );
  console.log('');
}

console.log('Loop stopped!');
```

### Declaring array

```javascript
const fruits = ['apple', 'orange', 'mango'];
fruits.length;
console.log('The lenght of this array is ', fruits.length);
console.log('This array: ' + fruits);

```

### ParseInt() and ParseFloat()

```javascript
parseInt("100") //  100
parseInt("3.14") // 3
parseFloat("3.14") // 3.14

```



### Declaring function

```javascript
function sayHello(name) {
  cosole.log('Hello '+name);
}

sayHello('Tomasz');
```

```javascript
const sayHello = (name) =>
{
	cosole.log("Hello "+name);
}

sayHello(“Tomasz”)
```

### Declaring function as an arrow function

In our project we are using most the time arrow functions! As you see above arrow function is the same as the usual function in JS.

```javascript
const sayHello = (name) =>
{
	cosole.log("Hello "+name);
}

sayHello(“Tomasz”)

```

### Destructing

```javascript
const myJson =  {
  id: 34243,
  title: "myTitle",
  published: 1999
  genreIds: [9,33,3,32,44]  
};

const {title, id, published} = myJson;
console.log(title);
// "myTitle"
const [,second] = myJson.genreIds;
console.log(second);
const [first, ,...others] = myJson.genreIds;
console.log(others);
// 3,32,44
```

### Destructing nested object

```javascript
const myJson =  { [
  id: 1,
  title: "myTitle",
  published: 1999
  genreIds: [9,33,3,32,44],
  id: 2,
  title: "myTitle2",
  published: 1992
  genreIds: [9,33,3,32,44],                            
};

const {, {title}} = myJson;
console.log(title);
// "myTitle2"
```

### 

### Default parameters

```javascript
function divide(a, b = 1) {
    return a/b;
}
```

### Spread

```javascript
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers));
//6
```

### REST

it is 3 dots. It collects all arguments into an array

```javascript
function sum(...myArguments) {
  return myArguments.reduce((total, curVal) => {
      return total+curVal;
  });
}

sum(1,2,3)
//6

function getArtistDetails(firstName, lastName, ...albums) {
	console.log(firstName);
 	console.log(lastName);
    console.log(albums);
}
getArtistDetails("Wiejski", "Wacek", "Szalala Szalala", "Orka Orka", "i takie tam inne przeboje")
//6
```

### 

### Anonymous function

```javascript
const greetMe = function() {
  console.log('hi');
};

greetMe();
```

### Anonymous function as an arrow function

```javascript
const greetMe = () =>{
  console.log('hi');
};

greetMe();
```

### Objects

You can see an object as a such block of values

```javascript
const person = {
  firstName: 'Tomasz',
  lastName: 'Krajewski',
  greet: function() {
    console.log('Hello '+this.firstName + ' ' + this.lastName);
  },
};

person.greet();

console.log(person.firstName);
console.log(person['firstName']);

```

remember you can get your object value in the two ways:

```javascript
person.firstName
```

or

```javascript
person['firstName']
```

### Objects shortened 

You can see an object as a such block of values

```javascript
const person = {
  firstName: 'Tomasz',
  lastName: 'Krajewski',
  greet () {
    console.log('Hello '+this.firstName + ' ' + this.lastName);
  },
};

person.greet();

console.log(person.firstName);
console.log(person['firstName']);

```

remember you can get your object value in the two ways:

```javascript
person.firstName
```

or

```javascript
person['firstName']
```

### Keyword this 

You can see an object as a such block of values

```javascript
const person = {
  firstName: 'Tomasz',
  lastName: 'Krajewski',
  greet () {
    console.log('Hello '+this.firstName + ' ' + this.lastName);
  },
};

person.greet();

console.log(person.firstName);
console.log(person['firstName']);

```



### Node api

https://nodejs.org/api/index.html

```javascript
const util = require('util');
const greeting = util.format('Hello, %s', name);
util.log(greeting);

```

### Class example

```javascript
class Person {
  constructor(firstname, lastname) {
    this.firstname = firstname;
    this.lastname = lastname;
  }

  greet() {
    console.log('Hello '+ this.firstname);
  }
}
const user = new Person('Tommy', 'Boby');
console.log(user);
```



### Getters and Setters

```javascript
class Person {
  constructor(firstname, lastname) {
    this._firstname = firstname;
    this._lastname = lastname;
  }

  greet() {
    console.log('Hello '+ this.firstname);
  }
  get firstname() {
      console.log("Getting name")
      return this._firstname;
  }  
    
  set firstname(newName){
      this._firstname = newName;
  }
    
}
const user = new Person('Tommy', 'Boby');
console.log(user);
user.firstname = "Frank";
console.log(user.firstname);
```

### Inheritance

```javascript
class Teacher extends Person {
  constructor(teachingSkills) {
	// super needs to be called first
    super();
    this._teachingSkills = teachingSkills;
  }
  // this set will run first and once for Teacher  
  set firstname(newName){
    console.log('It runs for Teacher')  
    this._firstname = newName;
  }
    
}
const user = new Teacher('Tommy', 'Boby',5);
const user1 = new Person('Arne', 'Resing');
console.log(user);
user.firstname = "Frank";
console.log(user.firstname);
```



### Declaring Objects

```javascript
const o1 = new Object();
const o2 = {};
const user = {name: 'tom', surrname: 'Kraj'};
```

You can add easily attributes:

```javascript
const user = {name: 'tom', surrname: 'Kraj'};
user['favFruit'] = 'bannana';
console.log(user);

// result: { name: 'tom', surrname: 'Kraj', favFruit: 'bannana' }

console.log(Object.keys(user).length);

// result: 3
```

### How to declare arrays:

```javascript
let arr= new Array();
let arr2 = [];
```

### How to check array?

```javascript
const arr= new Array();
const arr2 = [];
console.log(Array.isArray(arr));

// true
```

### Add a new element to an array:

```javascript
const arr2 = [];
arr2.push('abc');
console.log(arr2);

// [ 'abc' ]
```

### Iteration

```javascript
const user = {name: 'tom', surname: 'moni'};

for (let key in user) {
  console.log(key);
}

// name
// surname
```

### "for" loop

```javascript
const myArray = ['ala', 'ma', 'kota'];
for (let i=0; i<myArray.length; i++ ) {
  console.log(myArray[i]);
}

// ala
// ma
// kota

```

### Easier "for" loop

```javascript
const myArray = ['ala', 'ma', 'kota'];
for (value of myArray ) {
  console.log(value);
}

// ala
// ma
// kota

```

for objects

```js
const users = [{name: 'tom', surname: 'moni'}, {name: 'Tommy', surname: 'Moni2'}];

for (let user in users) {
  console.log(keyr.name);
}
```



### for each

accepts a callback function. Calls the function once per element in the array.

```javascript
const myArray = ['ala', 'ma', 'kota'];
myArray.forEach((value, index) => {
    console.log('Value: '+value);
    console.log('Index'+index);
})

```

for objects

```js
const users = [{name: 'tom', surname: 'moni'}, {name: 'Tommy', surname: 'Moni2'}];

users.forEach( function (user) {
 console.log(user.name);   
}
)
```

### Map

creates a new array with the results of calling a callback on every element in the array

```javascript
const myArray = ['ala', 'ma', 'kota'];
const myArrayUpper = myArray.map( (t) =>
                    return t.toUpperCase();
)
myArrayUpper.toString()
// ALA
// MA
// KOTA
const numbers = [1, 2, 7];

const buildObjectNumbersDetails = numbers.map( num => {
    return {
        value: num,
        isOdd: num %2 ==! 0
    }
}
)

```

### Array.find

```javascript
let names = {
    "Krajewski", "Dirk", "Dr Resing", "Prof Matloka", "Dr Szyszka"
}

names.find (name => {
	return name.includes('Dr')    
}
)
// it returns true when it ocurres first value of Dr



```

### Array.filter

```javascript
let names = {
    "Krajewski", "Dirk", "Dr Resing", "Prof Matloka", "Dr Szyszka"
}

const shortNamesLength = names.filter(name => {
	name.length<5;    
}
)
// it returns only Dirk

const middleNamesLength = names.filter(name => {
	name.length<5 && name.length>9;    
}
)

const allScientists = names.filter(name => {
	name.includes('Dr');    
}
)

```

### Array.Of

```javascript
const myArray = Array.of(8, [44,3,2,2], {sport: 'value'})

```

### Array.fill

```javascript
const myArray = [1,2,3,4,5]
myArray.fill("a", -2)
// [1,2,3,'a','a']
```



### loop for objects

```javascript
const user = {name: 'tom', surrname: 'Kraj'};
for (let value in user ) {
  console.log(value);
}

```



### Primitives

string, number, boolean, null, undefined, symbol

We copy the values

BUT Objects are stored by references!!

```javascript
const user = {name: 'tom', surrname: 'Kraj'};

let newUser = user;

newUser.age = 19;

console.log(user);
//{name: 'tom', surrname: 'Kraj', age: 18};
console.log(newUser);
//{name: 'tom', surrname: 'Kraj', age: 18};
```



### Callbacks

callback is a function passed to some other function, which we assume will be invoked at some point. The function “call back” invoking the function you give it when it is done doing its work.

the function I invoked will invoke function I will give

```javascript
function printUpper(myString) {
  console.log(myString.toUpperCase());
}
function printNumber(myNumber) {
  console.log(myNumber);
}
function run(callback, input) {
    callback(input);
    
}

run(printUpper, 'Hellooooo')
```



another example:

```javascript
function greet(callback) {
  console.log('Hello');
  const data = {
    name: 'John',
  };
  callback(data);
}

greet(function(data) {
  console.log('the callback was invoked');
  console.log(data);
});
```

the function I invoked will invoke function I will give.

```
### Files

We can use synchronous convention:

​```javascript
const fs = require('fs');

// it reads binary data
const greet = fs.readFileSync(__dirname+ '/hej.txt', 'utf-8');

console.log(greet);
```

Do you see differences with asynchronous example? What will happens if you call greet variable? If you have checked both examples and you know why you got undefined in the second one you can read next pages ;)

```javascript
const fs = require('fs');

const greet = fs.readFile('hej.txt', 'UTF-8', function(err, data) {
  console.log(data);
});

console.log(greet);
//undefined WHYYYYYYYYYYYY???
// Repeat That
```

**Error-first callback**: Callbacks take an error object as their first parameter
null if no error, otherwise will contain an object defining the error. This is a standard so we know in what order to place our parameters for our callbacks.

### Asynchronous programming

If you didnt understand first example with file reading just relax and try to understand how asynchronous work.
let's take a look on php code which can be equivalent to any your well known language like java or python. Whatever ;)

setTimeout function is a function which has 2 arguments: a callback and a delay
setTimeout(callback, delay) = 2 argument

```javascript
setTimeout( () => {
  console.log('The last, or the first one?');
},
4000);

setTimeout( () => {
      console.log('Should I be the first??');
   },
   0);
console.log('or me?');
```

Before you execute code, ask yourself what you get from the console first?
Easy because it was still something in the event queue. Using method setTimeout you registred 2 callbacks:
1 with console.log "I have done my work" and the second "Should I be the first??"

hej.txt

```
Repeat That
```

```javascript
const fs = require('fs');

fs.readFile('hej.txt', {encoding: 'utf8'}, function(err, data ) {
  if (err) {
     console.log(err);
  }

  console.log(data);
  fs.appendFile('hej.txt', data, (err) => {
    if (err) {
      if (err) {
        console.log(err);
        return;
      }

      console.log('OK');
    }
  });
});
```

After that you should see:
hej.txt

```
Repeat That
Repeat That
```

another example:

```javascript
setTimeout(

    () =>
    console.log("Line 1, 0 timeout"), 0);

console.log("line 2");
setTimeout(

    () =>
    console.log("Line 3, 100 timeout"), 100);

for(let i = 0 i<1000; i++){
    if(i==1000) console.log("Done");
}
```



another example:



1. Lets prepare something like that to show how callback works. We get userObject

```javascript
var getUser = (id, callback) => {
	var user = {
		id: id,
		name: 'Tom'
		};
		callback(user);
	};

getUser(31, (userObject) => {
	console.log(userObject);
});
```

2. and now lets add a real world case that we need to wait 5 sec for our user...

```javascript
var getUser = (id, callback) => {
	var user = {
		id: id,
		name: 'Tom'
		};
		setTimeout(
		()=> {
		callback(user);
		}, 5000);


	};

getUser(31, (userObject) => {
	console.log(userObject);
});
```

## Promise

The promise as an abstraction which tries to cover asynchronous programming and make your life easier. Imagine that  It promises you that you get a "gift" but you don't know when it happens and if it whenever happens but at the end you will get an answer if your promise was kept or not.

There are 3 states of promises:

- **Pending**, when the final value is not available yet. This is the only state that may transition to one of the other two states.
- **Fulfilled**, when and if the final value becomes available. A _fulfillment value_ becomes permanently associated with the promise. This may be any value, including `undefined`.
- **Rejected**, if an error prevented the final value from being determined. A _rejection reason_ becomes permanently associated with the promise. This may be any value, including `undefined`, though it is generally an error
  First simple example

Promise is a constructor with 2 callbacks. Resolve and reject but you can cal them as you wish

```javascript
var somePromise = new Promise( (resolve, reject) => {
	resolve('Hey. It worked!');

});
```

```javascript
somePromise.then( (message) => {
	console.log('Success:' + message);
});
```

Lets take a look at the code:

```javascript
const promisedPresent = getPresent();
promisedPresent
  .then(present => console.log('A nice gift!!', present))
  .catch(error => console.log('Sorry, no gift for you :(', error))
```

Function getPresent will be executed only if promise will be done with resolve state. If not you will get an error from catch. What is interessting for us... you don't know when it happens. It can be in 1 sec or 5 minutes.

```javascript
function getPresent() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve('After 5 seconds you got your gift, are you happy!');
    }, 5000); // 5 sekund
  });
}
```

Let see an other example.

Imagine you meet a girl who you really like. But you dont know if she likes you. You want to invite her to a cinema on Valentine's day but you need to get first if she likes you. You would never buy first ticket before you ask her out. Please check your code in the console.

You can treat setTimeout function like a time for thinking.

```javascript
const expectedAnswerfromMoni = 'Moni: I was waiting for that ages. Of course';
const expectedAnswerfromMoni2 = 'Moni: With pleasure my beloved';
const expectedAnswerKino = 'Kino lady: Yes we have 2 tickets for tonight movie: One Flew Over the Node.js Nest ';
const expectedKiss = 'Moni: Kiss Kiss Kiss. Only for you my hero!';


const yourAsynchronousTask = (expectedAnswer, reactionTime) => {
  return new Promise((resolve, reject) => {
    setTimeout((err) => {
      if (err) {
        reject(expectedAnswer);
      }
      resolve(expectedAnswer);
    }, reactionTime); // 5 sekund
  });
};

console.log('You: Hey Moni, do you want to go out with me?');

yourAsynchronousTask(expectedAnswerfromMoni, 4000).then((result) => {
  console.log(result);
  console.log('You: Do you want to go with me to cinema tonight?');
  return yourAsynchronousTask(expectedAnswerfromMoni2, 6000).then((result) => {
    console.log(result);
    console.log('You: I wasnt sure you want to go but I can call cinema right now');
    return yourAsynchronousTask(expectedAnswerKino, 10000).then((result) => {
      console.log(result);
      console.log('You: Hey Moni, should I get something from you?');
      return yourAsynchronousTask(expectedKiss, 1000).then((result) => {
        console.log(result);
      });
    });
  });
}).catch((error)=>{
  console.log(error);
});

console.log('But in the same time I can do other things!!!');
console.log('I take a look at her eyes');
console.log('Smile to her and so on');
```

But you can think... what happens when Moni say anytime no for your question! Our code wont execute after first "no" and you will get error message.

An another simple example:

In this time you can treat setTimeout function like any asynchronous call like calling database or any API

```javascript
const asyncAdd = (a, b) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (typeof a ==='number' && typeof b ==='number') {
        resolve(a+b);
      } else {
        reject('you can sum number and string!!');
      }
    }, 3000);
  });
};

asyncAdd(5, 10).then((res) => {
  console.log(res);
  return asyncAdd(res, 10).then((newResult) => {
    console.log(newResult);
    return asyncAdd(newResult, '2').then((nextResult) => {
      console.log;
    });
  });
}).catch((error) => {
  console.log(error);
});
```

As you saw in the last example you can can join so many promises as you want.

But you can chain so many then as you wish:

```javascript
getPresent()
  .then(present => returnToTheShop(present))
  .then(returnedMoney => buyNewiPhone(returnedMoney))
  .then(iPhone => iPhone.openTypeOfWeb());
```

To manage promises you can use an external module:
https://github.com/axios/axios



## Async

requires at least node 7.6

if you write "async" before function you just telling that this function depends on other asynchronous function. 

## Generators 

   you can compare generators to analog camera. If you take a picture the next is prepared

```javascript
function* aGenerator(){
  console.log('I ran once')
  yield 1; // Pause here and wait 
  console.log('I ran once')  
}
const gen = aGenerator();
gen.next();
gen.next();
gen.next(); 
```

## ES7

1. Exponentiation:

```javascript
const x = 3*3*3;
const x3 = 3**3;
```

2. Includes: returns true or false

```javascript
const arr = [0,2,3,4,555]
console.log(arr.includes(2))
```



### Error handling

if you get use to syntax try catch… you need to forget it for NodeJS. Pattern in Node.js

```
do_something (par1, par2, par3, (error, result) =>{

	if (error){
	SOMETHING BAD HAPPEND HERE!
	}

	else{
	do your stuff
	}

});
```

Sources:
https://www.tutorialspoint.com/javascript/

## Node.js <div id='id-section2'/>

Source: https://www.tutorialspoint.com/nodejs/

Node.js is a very powerful JavaScript-based framework/plattform built on Google Chrome's JavaScript V8 Engine. It is used to develop I/O intensive web applications like video streaming sites, single-page applications, and other web applications. Node.js is open source, completely free, and used by thousands of developers around the world.

## Features of Node.js

Following are some of the important features that make Node.js the first choice of software architects.

- Asynchronous and Event Driven − All APIs of Node.js library are asynchronous, that is, non-blocking. It essentially means a Node.js based server never waits for an API to return data. The server moves to the next API after calling it and a notification mechanism of Events of Node.js helps the server to get a response from the previous API call.
- Very Fast − Being built on Google Chrome's V8 JavaScript Engine, Node.js library is very fast in code execution.
- Single Threaded but Highly Scalable − Node.js uses a single threaded model with event looping. Event mechanism helps the server to respond in a non-blocking way and makes the server highly scalable as opposed to traditional servers which create limited threads to handle requests. Node.js uses a single threaded program and the same program can provide service to a much larger number of requests than traditional servers like Apache HTTP Server.
- No Buffering − Node.js applications never buffer any data. These applications simply output the data in chunks.
  Why Node.js is so fast because it uses machine code which is low level code that your computer can run directly without needing an interpreter.

## Environment:

If you use my VM nodejs is already installed. If you decided to use your own PC, please download latest version of Node.js https://nodejs.org/en/download/

## First Steps

### Hello world

Create a js file named hello.js on your machine having the following code.

```bash
$ echo console.log("Hello World")  > main.js
```

Now execute main.js file using Node.js interpreter to see the result:

```bash
$ node main.js
```

If everything is fine with your installation, this should produce the following result:

```
Hello, World!
```

### Create a project

Create a new directory

```bash
$ mkdir myFirstNodeProject
$ cd MyFirstNodeProject
```

With npm init you create a new node.js project with package.json that defines all properties of the project. It walks you through the properties and asks you one by one how to specify them. You can choose the default settings by clicking enter.

```bash
$ npm init
```

![npm init](https://lh3.googleusercontent.com/-tSviVQvQQvG9Dzb2LtAajfo0p7R2AxIztmRKUr3KSJN1haKM7rBPUYhu08URltlahXfNVPViOw)

### package.json

package.json is present in the root directory of any Node application/module and is used to define the properties of a package. Let's open package.json of my template skill:

```json
{
  "name": "My-template",
  "version": "0.0.1",
  "description": "Quickstart template for a NodeJS Application, you can easily deploy it in heroku",
  "engines": {
    "node": "6.9.4"
  },
  "main": "dist/app/index.js",
  "scripts": {
    "start": "node dist/app/index.js",
    "heroku-deploy": "git checkout atomic-development && git add ./ && git commit -m \"development increment\" && git push heroku atomic-development:master --force && heroku logs --tail",
    "serve": "node dist/app/index.js"
  },
  "repository": {
    "type": "git",
    "url": "t"
  },
  "keywords": [
    "nodejs"
  ],
  "author": "Tomasz Krajewski",
  "contributors": [
    {
      "name": "Tomasz Krajewski",
      "email": "Tomasz.Krajewski@opitz-consulting.com"
    }
  ],
  "license": "MIT",
  "devDependencies": {
	"alexa-verifier": "^0.3.6"

  },
  "dependencies": {
    "alexa-sdk": "^1.0.10",
    "aws-lambda-mock-context": "^3.1.1",
    "body-parser": "^1.17.2",
    "botkit": "^0.5.4",
    "express": "^4.15.3",
    "request": "^2.81.0",
    "mongoose": "^4.10.5",
    "mongodb": "^2.2.26",
    "ip": "1.1.5",
    "local-ipv4-address": "0.0.2"

  }
}

```

Thanks package.json you are able to install all node.js modules. For example if you like to add the dependency request to do API calls, you need only to use the following command and the request module will be added to your project. Parametr --save will ensure that your module will be added to package.json

```bash
$ npm install request --save
```

![enter image description here](https://lh3.googleusercontent.com/riwdB6g1lWULXXQu6GaK7FaCk6r8JvySAkqQrJnHSGsmq6gliSaXeXJ9TvLCa0PH-TJNMKD3qYQ)
All required modules from package.json will be saved to your project directory. The file package.json now contains the dependency request.
![enter image description here](https://lh3.googleusercontent.com/O7KM53-AhCm6GAiie9DS-VRKObytbWwGOJTuRdNp8AOtFP-YN2bbRJ8y-KZxfUWsFyIt-nHlfOs)

## Arrow function

An arrow function is defined using a pair of parentheses that contains the list of parameters (param1, param2, ..., paramN), followed by a fat arrow => and a pair of curly braces {...} that delimits the body statements.
When the arrow function has only one parameter, the pair of parenthesis can be omitted. When it contains a single statement, the curly braces can be omitted too.

The following example shows the arrow function basic usage:

```javascript
var absValue = (number) => {
  if (number < 0) {
    return -number;
  }
  return number;
}
absValue(-10); // => 10
absValue(5);   // => 5
```

absValue is an arrow function that calculates the absolute value of a number.
The function declared using a fat arrow has the following properties:
The arrow function does not create its own execution context, but takes it lexically (contrary to function expression or function declaration, which create own this depending on invocation)
The arrow function is anonymous: name is an empty string (contrary to function declaration which have a name)
arguments object is not available in the arrow function (contrary to other declaration types that provide arguments object)

but you can do something like this too!

```javascript
var squer= (number) => number*number;
squer(10); // => 100
```

## Module

lets take a look at an example:

apps.js

```javascript
const fs = require('fs');
const os = require('os');
var user = os.userInfo();
const notes = require('./notes.js');

fs.appendFile('greetings.txt', 'Hello '+user);

```

notes.js

```javascript
console.log(module);

```

output:

```javascript
Module {
  id: 'C:\\aprivat\\Node Tutorial\\notes.js',
  exports: {},
  parent:
   Module {
 	id: '.',
 	exports: {},
 	parent: null,
 	filename: 'C:\\aprivat\\Node Tutorial\\app.js',
 	loaded: false,
 	children: [ [Circular] ],
 	paths:
  	[ 'C:\\aprivat\\Node Tutorial\\node_modules',
    	'C:\\aprivat\\node_modules',
    	'C:\\node_modules' ] },
  filename: 'C:\\aprivat\\Node Tutorial\\notes.js',
  loaded: false,
  children: [],
  paths:
   [ 'C:\\aprivat\\Node Tutorial\\node_modules',
 	'C:\\aprivat\\node_modules',
 	'C:\\node_modules' ] }
```

So let's use this exports object
apps.js

```javascript
const fs = require('fs');
const os = require('os');
var user = os.userInfo();
const notes = require('./notes.js');
console.log(notes.myNote);
fs.appendFile('greetings.txt', 'Hello '+user);
```

notes.js

```javascript
module.exports.myNote = “Hello”;

```

**Excercise 1**:
What did you see in the output?

The real goal is exports functions that we can use in app.js
Lets change notes.js
notes.js

```javascript
module.exports.myNote = () => {
 return "my note";
}
```

and app.js

```javascript
const fs = require('fs');
const os = require('os');
var user = os.userInfo();
const notes = require('./notes.js');
notes.myNote();
fs.appendFile('greetings.txt', 'Hello '+user);
```

If you want to use variables as a module you can just declare it in your variable in a JS script file:

```javascript
const helpers = require('./greet');

console.log(helpers.greet);
console.log(helpers.otherGreet);

```

Exports module

```javascript
const greet = 'Hello from me!';
const otherGreet = 'Hello from other side';
module.exports = {greet, otherGreet};
```

## Blocking Code vs non blocking code example

The most weird thing with nodejs is to understand non blocking code. Please compare 2 examples:

Create a text file named hej.txt with the following content :

**hej.txt**

```javascript
This is an example from Tutorials Point is giving self learning content
to teach the world in simple and easy way!!!!!
```

Create a js file named blockingCode.js with the following code −

```javascript
const fs = require('fs');

const data = fs.readFileSync('hej.txt');

console.log(data.toString());
console.log('Program Ended');
```

Now run the main.js to see the result −

```
$ node main.js
```

Verify the Output.

It was a blocking code example.

## Non-Blocking Code Example

Create nonBlockingCode.js

```javascript
const fs = require('fs');

fs.readFile('hej.txt', function(err, data) {
  if (err) return console.error(err);
  console.log(data.toString());
});
console.log('Program Ended');
```

Now run the nonBlockingCode.js to see the result −

```
$ node nonBlockingCode.js
```

These two examples explain the concept of blocking and non-blocking calls.
The first example shows that the program blocks until it reads the file and then only it proceeds to end the program.
The second example shows that the program does not wait for file reading and proceeds to print "Program Ended" and at the same time, the program without blocking continues reading the file.
Thus, a blocking program executes very much in sequence. From the programming point of view, it is easier to implement the logic but non-blocking programs do not execute in sequence. In case a program needs to use any data to be processed, it should be kept within the same block to make it sequential execution.

character encoding: how characters are stored in binary. The numbers (or code points) are converted and stored in binary.

## DEBUGGER

This solution is only for remote code like in

```
node inspect-brk [filename.js]
```

Open for example WebStorm or any JS IDE supporting debug mode and connect to the debugger

In Webstorm click in the buttom toolbar Run-->Edit Configurations
Please choose from templates: "Attach to Node.js/Chrome"
In the host add ip address of your docker-machine. In my case **localhost** or any ip address where your app is hosted

![enter image description here](https://lh3.googleusercontent.com/tHxcCnHN6wc4Qg7FM-WqsBrnUpqaXrEpYsRyWY2_eBYy3N3OulflFn_eTtg_ikTJHSbdrFal3Ij7sr84XyTCXsed59h8yDthnsG5olrGG4t78vrcINhxuGEBs9p_62vWZlMstMaEAwh6oo8UEj60UAueE-Z3AJ427lJKXaNhYXVDIDn-XRa0svnhyeqoSfqvOZqZiJGmNVaKQ9JIWvAZsJvCyy2gwWAabP-7BvYCxu5oW4vCn9e6tFlCPxY8qPUhAU7LeJJH4d4wZ1T8kWpvf_G6lkOhheXjMgdaammQYd3PgcUtpCE8XbxaMq45rhknXX8Z-f-XgmKkoSjbTors2BhAq7vWWY2_Nwlwks18Mfvn2nyEUe1cTHqEnoUj3oQCJTeuMH9cPzpwyE67GGM0Pl1QZpnlIZv__HWMPa9O00rwITVflVUr09DcECKaNARjNW8OVM8SMoe9A-QBn49YTUObZ_MSPu1BX_xRpW9GdJ-BzqztrbaMQR9hAMbGxGP6B_n6iD0TWC92QkjeV0zqkVFBX4YKzoOWQxSV15agUYKPCFM2KpG_rJ1YtnWPCNOMR0PjJUzzdz44bdu0vh_60N78ZP1OV6j8BkXymOrdBvtTxv_X7uKtrtpJF1VgcbZzzPE9ahnGTlYRvtUAgJNw0zfNSkoxcvddE8MolHNTYk7b1Hq0BDk2G4bQvfOgPFhm_oGIEavzkz7uGR3hlA=w1346-h841-no)
and click apply and **+** button in the left button corner

![enter image description here](https://lh3.googleusercontent.com/Bss0hviB3jsPljLWRodBulNb3aOZE0X3SXwf1-Bf5K7VgeQOCh1xwi3yVPmp3_IMKrDIKZgu27_zH3orh3Vlwn-QexQFPzlcamP-zihZpuleaKa-MFy4Or0285VnWtkc1M_9Xj9Xbg6AJY4gnA1vEHPAi8HobQT8X2l13P796INCRhjd7hqNs442qsgJKXwjkLCX1Y04__FRHOE3ywH26rdg8u3-KVefsfAQgE5hcDRWsq5sq-TLM7nSaz0-AsK9_3uNiyHlT_mIsGMSYcqVEO1usyIAhUJe79DEPGHjUM0ONqorHKzaw9L1oXMDgxCkoLVKxnGAj_Ccu-X6mxRxj8cU0ExTHoBQtD5yZ2lVWP-N4R4RuUeLJ_Wo4ZPg0AxU3zP_A5PXHIUqTBptF1d199URQOV7ps68KbeiRhvUffWLwyzcaId--yLsDXn9ID1ZEUSSHiH8W8ztxZlMKx1ENjTTcIKPED8j911t_o-vEiiycjjIU_nq6bkHywFy3oUqjcsb98Hw2LwEIBo7Hb2HyXAwNQbhgXlpzIvcC_6qbogGVr3gxUSf8itbZPP5wffnGJ9T8huAZw-MdVbIPhd_c6A47wft9uu_RCn_Ya1Anrd99fEfkgUH6LLbpfDiDYdEYX31F6j2W5oEGCptzva-0DO24S2YIvwNrsoGa62yy8LfNd5gZ0ebDZMxZ-nrFW1doFTQoyLLprb2mrFtNw=w1145-h299-no)

Now if you click Run-->You can run your defined debug process

You can add your first breakpoint clicking to a choosen line and start conversation from DialogFlow.
You can see your debugged code in the WebStorm console.

![enter image description here](https://lh3.googleusercontent.com/_RGQbo9Hw3Bk53SgNFH1lZLYbi5eK8TVmbhsf9Le6bQZmJ7AYCCOFPsHgzvzyFWcxLlghsqm0tmvEp2aiakwebuLx-SEW0onBDdr9w96--Fdd5C9Ja-Qx3tu1eLd6REIFdm7robfx2PLEa4jOyyttmlfxyPMx30D2h5EAAt4APUu0rYMKcHMIxNz171Wrqy4iMcoPpSMV-8PuqEwklViBkVZvi0xrsDyyxnFQlghBYqwfyg7go57TwIPTfbxnPYJDJxivy_XHOu-x2HPl1OwgS0kIBPVF0e8HSflw28PqKxVl3YbFdhe3gp8OOdWfE-HQaul8CaJjH77dJ8eliucTBHJIqnyLHuAjemqcG_JTLNAJeKlLng4OuJLRZIPTJbK2h0BYWeOWk7mAnlqSoi-cTcWrODVmReRUAqmNYM8Lk-3zJSDtYi1gHOXaWRTzyV99y0Pfb4ZSsJ9nvAke4evQc94cIaUpdswWCj6BvAi_U0IpEzMbtgw24fvIh72k4nA_4HM_cYAfheXgzjCEJTk9eLYwRA0TwvcuUBCWLGV8J_0pzNN0yMmL_1S3ToTTPKKfMH82nNS-IHD9b92tWXnDpVcrj4R7CNs2Jq4mAk_MTZtQ8wxeDhbjj6woFj0fQI_TYFfn_t79JJA-3d9ulqyM9WjHmYIrXWgNb5oKuKuzKLSqNOOnXi64PU4YQsuvfoXBu_04c2eOriqP7bsCA=w1771-h679-no)

Sources:
https://www.tutorialspoint.com/nodejs/