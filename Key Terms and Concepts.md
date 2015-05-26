#Key Terms and Concepts

######1) List and describe each of the primitive data types (number, string, boolean, null, undefined). What do they each represent?

number- represents a numeric value. There are no commas once a number >= 1000; You can use negative numbers (-55), and use decimals (0.75).  

string- letters and other characters that are enclosed in quotation marks. The quotes can be single or double.
``` "Hello, world!" ``` is an example of a string. Strings are often used to add new content to a page. Note: if you want quotation marks to appear in your text, you need to use a backslash before any type of quotation mark that that is in the string. For example: "(I NEED A GOOD EXAMPLE)"

boolean- ```true``` and ```false```. Often in Javascript, boolean values act as an on and off switch for a function.

null and undefined- "There are two special values, written null and undefined, that are used to denote the absence of a meaningful value. They are themselves values, but they carry no information.Many operations in the language that don’t produce a meaningful value (you’ll see some later) yield undefined simply because they have to yield some value.The difference in meaning between undefined and null is an accident of JavaScript’s design, and it doesn’t matter most of the time. In the cases where you actually have to concern yourself with these values, I recom- mend treating them as interchangeable (more on that in a moment)." -Eloquent JS, p. 19


######2) What is a variable?

A variable is a letter, string of letters, or number that is assigned a value using the assignment operator (=). Unlike other languages, you do not have to specify what type of data a variable will hold.

``` var foo = 45;```

*"A variable is a good name for this concept because the data stored in a variable can change (or vary) each time a script runs." Duckett, p. 59.*

######3.  Describe in precise terms what’s happening with variable assignment using “var keyword”, “identifier”, “value”, “assign” etc…

*"Before you can use a variable, you need to announce that you want to use it. This involves creating a variable and giving it a name."* -Duckett, p. 60

var keyword- ```var``` is a a keyword in Javascript, and the program know that this keyword creates a variable.

indentifier-  a synonym for the variable name. In the following example: ```var converter```, ```converter``` is the identifier, or variable name. The identifier should describe the data the variable holds.

*"Once you have created a variable, you can tell it what information you wuld like it to store for you. Programmers say that you assign a value to the variable."* -Duckett, p. 61

value- the data type you would like the be assigned to the variable.

assign- ```=``` is an assignment operator. It stores the value on the right side of the expression, in the variable on the left side.


######4. Evaluate the following expression: !(typeof(9) === typeof(9.5) && (99 == "99" || !true))


The ```typeof``` operator returns a string which tells what type of data is in the parentheses

```!``` -> 'logical not'

```===``` -> 'strict equals'

```||``` -> 'logical or' texts at least one condition

```typeof(9) === typeof(9.5)``` is like asking "is number === number"? and will evaluate to ```true```

```&&``` ->  'logical and' texts more than one condition

```99 == '99'``` the ```==``` is asking for a "loose equals", and Javascript does a type coercion(?), and simply checks that the values match

a strict equals ```==``` check that the value and data types match

```||``` ->

not(true && (true or not true))

######5. Use a for loop to iterate through an array.
```var arr = ['cat', 'dog', 'chicken', 'duck', 'rabbit'];```

```for (var i=0; i <arr.length; i++){```
	```console.log(arr[i]);
}```

######6. Define functions using declarations and expressions.
*"To create a function, you give it a name and then write the statements needed to achieve its task inside the curly braces. This is known as a function declaration"* --Duckett, p. 90

```function sayHowdy (){
	return('Howdy!);
} ```

In the function above, ```function``` is the function keyword, which is Javascript's way of declaring a function.

The function has been defined as ```sayHowdy``` and  

*"An expression evaluates into a single value. ```var color = 'purple';``` The value of color is now purple"* --Duckett, p. 74

######7.  Articulate the difference between defining and invoking a function.

To define (declare) a function, you must use the ```function``` keyword, assign the function a name, and write statements telling the function what to do inside the curly braces.

example: ```function walkDog(arr) { code here}; ```

To call a function, you use the function name followed by parentheses.

example: ```walkDog(['Gamut', 'Rico');```

######8. Describe how data flows into a function using parameters and arguments.
*"If a function needs information to work, you indicate what it needs to know in parentheses after the function name." --Duckett, p. 92*

```function multiply (a, b) {return a * b;}``` The parameters are ``a`` and ``b``.

*"When you call a function that has parameters, you specify the values it should use in the parenthese that follow its name. The values are called arguments, and they can be provided as values or as variables."* -- Duckett, p. 93

Arguments can be provided as a value. For example,

``multiply(3,5)``

Arguments can be provided as variables. For example,

`` a = 10;``

   ``b = 5;``

  ``multiply (a,b); ``

######9. Describe how data flows out of functions (by using the return keyword).

When you write a function, and you expect an answer to be produced, the reponse is a return value. ```return``` is a keyword.

######10. Explain the prhase "functions are just values."

A function has a variable name, an assignment operator, and a variable value. The function may need to complete some calcuations before it can return a value.

######11. Write a function that returns multiple values.

```function getSize(width, height, depth) {
  var area = width*height;
  var volume = width*height*depth;
  var sizes = [area, volume];
  return sizes;
}```

```var areaOne = getSize(3, 2, 3)[0];```

```var volumeOne = getSize(3, 2, 3) [1];```


######12. Write functions that have side effects, such as logging to the console or manipulating DOM.


######13. Explain the difference between locally-scoped and globally scoped variables and write examples of each.

A local variable is written inside of a function, and it can only be used within that function.

example: ```function getArea(width, height){
	var area = width * height;
	return area;
	}```

	```area``` is a local variable

A global variable is written outside of a function, and can be used anywhere in the Javascript document. Global variables are stored in memory for as long as the webpage is loaded, and they increase the possibility of naming conflicts. That is why declaring a global variable is called 'polluting the global scope.'


######14. Define ‘type coercion’ and identify instances when it occurs.
Type coercion is when Javascript converts one data type to another, like converting a string to a number.

*"If you use a data type JavaScript did not expect, it tries to make sense of the operation rather than report an error."*  --Duckett, p. 166

Because the language allows the data type for a value to change, JavaScript uses **weak typing.** Other languages that require you to specify which data type your variable is use **strong typing.**

######15. Explain the DOM. Where does it live? What is it for? How does it get created?

DOM stands for Document Object Model, and it tells browsers how to create a model of an HTML page so that JavaScript can access and change elements. The DOM is an Application Programming Interface (API). APIs allow programs to communicate with one another.

######16. Describe the CSS Box model. What 5 properties affect the box model?

The box model refers to the reality that all elements on a page are contained in a rectangle. Each box size is affected by the margin, border, padding, and content.

######17. What is the difference between relative and absolute poitions in CSS?

Absolute position means that you fix an element to one place on the page, and it remains there regardless of other elements, and when the user scrolls up and down the page. The position starts at the top left part of the page.

Relative position means that you can "scoot" an element on the page. The element starts its position relative to the other elements on the page.

######18. What is the difference between block and inline elements?

Block elements take up the entire width of their container and force new lines, while inline elements take up only the width of their content, and do not force new lines.

######19. Explain each step of the basic git flow. What does each git command do?
######20. Git Branches: What are they? What are they used for?
######21. What's the difference between git and github?


######22. Identify all of the truthy and falsy values in JS and explain what it means to be “truthy” and “falsy”.

In JavaScript, developers sometimes use the loose equals ```==``` because it will return more values than strict equals. Developers use truthy and falsy values to check for the presence of an object or array.


######23. How do you access elements inside of an array?
In order to access an element inside of an array, you type the name of the array, and then use square brackets to specify the index number you want. This is called sub-notation.

For example

```var weather = ['rain', 'sun', 'wind']```

In order to access the value ```sun```, you would use ```weather[1]```

######24. What's the difference between arrays and objects?
An array is a numbered list of values.

*"Objects group together a set of variables and functions to create a model of something you would recognize from the real world.

In an object, variables become known as properties, and functions become known as methods."* --Duckett, p.100

```var gSchool = {
	name : 'galvanize full-stack',
	location: 'pearl street',
	people: 'g7 and g8',
	checkGraduate: function (){}
	};```

	the key value pairs are properties (variables), and the function is a method.

######25. How do you create arrays and objects?
To create an array, you declare a variable, and then assign it the value of an array using square brackets []. The values are separated by commas.

To create an object, you declare a variable, and then assign it the value of an object using curly braces {}. The key value pairs (properties) are separated by commas.

######26. How do you access values inside an object?
In order to access the values inside of an object, you can use dot notation, which means you type the nameOfObject.propertyToAccess;

You can also use sub-notation: nameOfObject['propertyToAccess'];

######27. Describe the three components of a for loop.
A for loop has three main parts:
```var i = 0;``` This is the counting variable, and tells the computer to start at the index of 0.

```i < arr.length``` This tells the computer where to stop counting. In this example, the loop will stop once it has counted every item in the array.

```i+=3``` This is the incrementor, and tells the computer to increase or decrease by this amount while counting.

######28. What are JS events? Give an example.
JavaSrcipt events are the browser's way of saying, 'I just noticed something (like a click, or mouseover) just happened!"

These events can trigger code that is interesting to user.s.

######29. What is event propagation?
Even propogation is a JavaScript behavior in which events bubble up from their decendents to their ancestors. In order to stop this, you can use the method ```.stopPropagation()```

######30. What is npm?
NPM stands for Node Package Manager.
"npm makes it easy for JavaScript developers to share and reuse code, and it makes it easy to update the code that you're sharing." --[Click here!](https://docs.npmjs.com/getting-started/what-is-npm)
######31. What are npm modules? How do you install an npm module?
?



######32. Describe the execution of a while loop and the potential for infinite loops.
If you don't tell when the while loop to stop counting, it will go on forever.
