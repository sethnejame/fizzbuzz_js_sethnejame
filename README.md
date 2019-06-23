### Question 1: In your README.md, to the best of your knowledge, please explain what the following lines of code do: global.browser = new BrowserHelpers(), global.expect = chai.expect;

Both 'BrowserHelpers' and 'chai' are constants declared just prior to the referenced code.  'BrowserHelpers' requires 'e2e_training_wheels' which refers to our particular testing suite and 'chai' requires 'chai' which is an additional test driven development library.  When we declare these two constants w/ global scope, we are telling Node that we want to include Chai and E2E as part of our testing framework/process.

### Question 2: In your README.md, to the best of your knowledge please explain why we are placing the let fizzBuzz = new FizzBuzz outside the it block?

We need to instatiate a new FizzBuzz function (named 'fizzbuzz') so that we have something to test.  Otherwise we will be testing a function that hasn't yet been called.

### Question 3: In your README to the best of your knowledge please explain the difference between using === and == in JS?

The double '==' and triple '===' are two different type of comparison operators.  The double equals operator just compares two items by value, for instance, the number 3 and the string '3' would be equal in JavaScript's eyes.  However, the triple equals operator is a strict value/type comparison, so the integer 3 and the string '3' would not be equal.  They would have to be of the same value (3) and type (either string or integer) to return true.