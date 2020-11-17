            Js learning outcomes 2

    • What are the eight data types of javascript? 
      
      The number type represents both integer and floating point numbers.
      Also pos & neg Infinity and NaN.
      
      BigInt type was recently added to the language to represent integers of arbitrary length.
      // the "n" at the end means it's a BigInt
      EG const bigInt = 1234567890123456789012345678901234567890n;
      A string in JavaScript must be surrounded by quotes.
      let str = "Hello";
      let str2 = 'Single quotes are ok too';
      let phrase = `can embed another ${str}`;
      The boolean type has only two values: true and false.
      This type is commonly used to store yes/no and comparison values: true means “yes, correct”, and false means “no, incorrect”.
      
      The special null value does not belong to any of the types described above.
      let age = null;
      It’s just a special value which represents “nothing”, “empty” or “value unknown”.
            The code above states that age is unknown.It forms a separate type of its own which 	contains only the null value:
	The special value undefined also stands apart. It makes a type of its own, just like nul 	The meaning of undefined is “value is not assigned”.                                                                 	If a variable is declared, but not assigned, then its value is undefined:                            	let age;                                               	alert(age); // shows "undefined"                        	Technically, it is possible to explicitly assign undefined to a variable:
	The object type is special. All other types are called “primitive” because their values can 	contain only a single thing (be it a string or a number or whatever). In contrast, objects are 	used to store collections of data and more complex entities.                                                  	The symbol type is used to create unique identifiers for objects. We have to mention it here 	for the sake of completeness, but also postpone the details till we know objects.
      The typeof operator returns the type of the argument. It’s useful when we want to process values of different types differently or just want to do a quick check – although there is a bit more to it than that!

            Summary
    • number
    • bigint 
    • string 
    • boolean 
    • null 
    • undefined 
    • object 
    • symbol 
    • typeof 
    • Which data type is NOT primitive? 
      The object type is not primitive and one day I might know why!
      
    • What is the difference between single, double, and backtick quotes for strings? 
      
      Single and double quotes are “simple” , ‘simple’, quotes and effectively the same.
      Backticks are more powerful and enable one to embed variables and expressions into a string.
      
    • Which type of quote lets you embed variables/expressions into a string? 
      
      Backticks 
      
    • How do you embed variables/expressions into a string? 

            This can be done for example with ${…} 
      as in  let name = “John”; 
      // embed a variable  
      alert  ( `Hello, ${name}!` );  //  Hello, John! 
      // embed an expression 
            alert (`The result is ${1 + 2}`);  //The result is 3

    • How do you escape characters in a string? 
      
	Characters that may confuse the presentation, for instance a quotation mark that would    	incorectly indicate the end of a string eg 
	alert (‘I’m the Walrus!’);  would result in a syntax error.
	Using  \  before the offending  ’  would correct the situation  
	alert (‘I\’m the Walrus!’);   // I’m the Walrus!
	
    • What is the difference between slice/substring/substr? 
      They are all methods for removing part of a string and showing it as a new string.
      Slice() can use positive or negative position values. If the end position value is left out this method will assume the remainder of the string is to be included.
      Substring() acts the same as slice() but cannot accept negative postion values.
      Substr()  again same as slice , can accept negative position values but the second value is the length of the string to be extraced and if left out will assume the remainder of the string to be extracted.
      
    • What are methods? 
      JS methods are actions that can be carried out on js objects.
      
    • What are the three logical operators and what do they stand for? 
	&& 	logical and 
	||	logical or
	!	logical not

    • What are the comparison operators? 
      
      Comparison operators test for true or false
      ==	equal to
      ===	equal to by value and type
      !=	not equal
      !==	not equal value or not equal type
      >	greater than
      >=	greater than or equal to
      <	less than
      <	less than or equal to
      
    • What is nesting? 
      
      Nesting is declaring a function within a function. Apparently used a lot in js. 
      The inner function is called by the outer function being called
      //a simple example, but this should get the point across... 
      function outerFunction(){ 
      console.log("I'm the outer function"); 
      function innerFunction(){ 
      console.log("I'm the inner function"); } 
      innerFunction(); } 
      outerFunction(); 
	I'm the outer function
      I’m the inner function
      
    • What are truthy and falsy values? 
      They are the inherent boolean values of  each variable value and will, when evaluated, result in true or false.
      There are some differences in the way different progamming languages evaluate some values.

    • What are the falsy values in JavaScript?
      the number 0,  the BigInt 0n,  the keyword null,  the keyword undefined,  the boolean false,
      the number NaN,  the empty string "" (equivalent to '' or `` ) . Differences will be seen in
      other languages.

    • What is the syntax for an if/else conditional? 
      if (condition) {
  //  block of code to be executed if the condition is true
} 
      if (hour < 18) {
  greeting = "Good day";
} 
      result:		Good day
      
      if (condition) {
  //  block of code to be executed if the condition is true
} else { 
  //  block of code to be executed if the condition is false
}
      if (hour < 18) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
      result: 	before 6pm is Good day
                       after 6pm is Good evening.
    • What is the syntax for a switch statement? 
      
	<!DOCTYPE html>
<html>
<body>

<p id="demo"></p>

<script>
let day;
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case  6:
    day = "Saturday";
}
document.getElementById("demo").innerHTML = "Today is " + day;
</script>

</body>
</html>

    • What is the syntax for a ternary operator? 
      
      <!DOCTYPE html>
      <html>
      <body>
      
      <p>Input your age and click the button:</p>
      
      <input id="age" value="18">
      
      <button onclick="myFunction()">Try it</button>
      
      <p id="demo"></p>
      
      <script>
      function myFunction() {
        var age, voteable;
        age = document.getElementById("age").value;
        voteable = (age < 18) ? "Too young":"Old enough";
        document.getElementById("demo").innerHTML = voteable + " to vote.";
      }
      </script>
      
      </body>
      </html>


      What is the relationship between null and undefined? 
      They have the same value but are of different types.
      Null is an object type whereas an undefined type is undefined.
      
    • What are conditionals?
      Conditionals enable decisions to be made whether pieces of code can run.
      A conditional statement tested against a variable value can result in a piece off code being run or not, or an alternative piece of code run instead.
      They are:
      if/else
      switch
      ternary
      



