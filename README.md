# FizzBuzz Challenge

The FizzBuzz Challenge was assigned as part of Week 2's problem set @CraftAcademy, Stockholm.  Students were tasked with
writing tests for and deploying a working FizzBuzz app with CSS styling.  Afterward, the app was deployed to GitHub pages.  The deployed app can be visited here: https://sethnejame.github.io/fizzbuzz_js_sethnejame/

## Exercise Questions

1. In your README.md, to the best of your knowledge, please explain what the following lines of code do: global.browser = new BrowserHelpers(), global.expect = chai.expect;

Both 'BrowserHelpers' and 'chai' are constants declared just prior to the referenced code.  'BrowserHelpers' requires 'e2e_training_wheels' which refers to our particular testing suite and 'chai' requires 'chai' which is an additional test driven development library.  When we declare these two constants w/ global scope, we are telling Node that we want to include Chai and E2E as part of our testing framework/process.

2. In your README.md, to the best of your knowledge please explain why we are placing the let fizzBuzz = new FizzBuzz outside the it block?

We need to instatiate a new FizzBuzz function (named 'fizzbuzz') so that we have something to test.  Otherwise we will be testing a function that hasn't yet been called.

3. In your README to the best of your knowledge please explain the difference between using === and == in JS?

The double '==' and triple '===' are two different type of comparison operators.  The double equals operator just compares two items by value, for instance, the number 3 and the string '3' would be equal in JavaScript's eyes.  However, the triple equals operator is a strict value/type comparison, so the integer 3 and the string '3' would not be equal.  They would have to be of the same value (3) and type (either string or integer) to return true.

4. In your README to the best of your knowledge please explain why we are moving (number % 5 === 0) to the top?

Some numbers are divisible by both 3 and 5, like 15 for instance.  The 'if' loop we currently have will execute the first condition that applies true.  So if the loop comes across the number 3 and the condition for 3 is first in line, "Fizz" will be printed and the loop will close, skipping the condition for 5.  For this reason we move the condition for 5 to the top so that numbers more commonly divisible by five (than 3) will print Buzz.

5. In your README to the best of your knowledge please explain the difference between feature and unit test

A unit test is for a small component or function to confirm that the desired output is correct.  A feature test is a collection of unit tests that produce an ultimate result, to confirm that a feature (comprised of multiple interconnected functions/methods/algorithms) is working properly.

6. In your README to the best of your knowledge please explain what this following code does

The first test is an async await function that tells the browser to open up and visit the local host address where our fizz buzz function is located.  The second test checks to make sure the browser reloads.  The last test closes the browser window after the testing is done.

7. In your README to the best of your knowledge please explain what expectations in the context of testing are

Expectations of any particular unit/feature test are the expected outcome or result of the test. If you have a function that compares two numbers and returns the larger of the two numbers, your expectation for that test would be the largest number of the two arguments.

8. In your README to the best of your knowledge please write a line to line explanation of what is happening in this code

```<script src="js/fizzbuzz.js"></script>```
This line includes the fizzbuzz.js file with our fizzbuzz function.

```    <script>```
```       document.addEventListener('DOMContentLoaded', () => { ```
These lines add an event listener to the DOM (document object model) that says 'Hey, when you've loaded, do the following: '

```            let button = document.getElementById('button') ```
Create a local var called 'button' and assign it to the button in the html page by ID.

```            let displayDiv = document.getElementById('display_answer')```
Grab the div inside the html page with the ID 'display_answer' and store it in the local displayDiv variable

```            button.addEventListener('click', () =>{```
Add an event listener to the button called 'button' that waits for a click

```                let value = document.getElementById('value').value```
Grab the input field with id 'value' and assign it to a local var called 'value'

```                let fizzBuzz = new FizzBuzz```
Instatiate the FizzBuzz function in a new var 'fizzbuzz'

```                let result = fizzBuzz.check(value)```
Store the return val of fizzbuzz in a local var called 'result'

```                displayDiv.innerHTML = result;```
Display the 'result' var inside the display div

```            })```
 ```       })```
```    </script>```

9. In your README to the best of your knowledge please explain what a CDN (Content Delivery Network) is?

A content delivery network is a network of servers that host a particular set of files/apps across the globe.  In theory, a user desiring said files/apps can link to them remotely and put them to use.  Because many servers host the same content, the idea is that the user will always be near a server in his/her area that hosts the content, making it easier to access/link to.
