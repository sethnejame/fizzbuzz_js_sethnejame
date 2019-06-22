### Question 1: In your README.md, to the best of your knowledge, please explain what the following lines of code do: global.browser = new BrowserHelpers(), global.expect = chai.expect;

Both 'BrowserHelpers' and 'chai' are constants declared just prior to the referenced code.  'BrowserHelpers' requires 'e2e_training_wheels' which refers to our particular testing suite and 'chai' requires 'chai' which is an additional test driven development library.  When we declare these two constants w/ global scope, we are telling Node that we want to include Chai and E2E as part of our testing framework/process.

### Question 2: In your README.md, to the best of your knowledge please explain why we are placing the let fizzBuzz = new FizzBuzz outside the it block?

We need to instatiate a new FizzBuzz function (named 'fizzbuzz') so that we have something to test.  Otherwise we will be testing a function that hasn't yet been called.