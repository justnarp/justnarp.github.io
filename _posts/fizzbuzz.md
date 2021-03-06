<a href="https://www.amazon.com/gp/product/B00PYBJ7DQ/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00PYBJ7DQ&linkCode=as2&tag=mikelothar-20&linkId=03232bbc905bad02f3a080458371f3d7" target="_blank"><img src="https://images-na.ssl-images-amazon.com/images/I/41y0gMLSgsL._SX312_BO1,204,203,200_.jpg" style="width: 50px; float: right;"></a>
FizzBuzz is a common test given to JavaScript candidates. Interesting enough, 
only around 1 in 200 get this right during the first try. I'll try to go through
a transformation of a common solution of FizzBuzz into a Functional Programming
solution, based on K. Anand Kumar's book '_The Magical World of Functional Programming: Part I_'.


## FizzBuzz
FizzBuzz, in all its simplicity, is a program that should do the following for all
numbers between 1 and 100 (both included):

* Print the `number` followed by the string "Fizz" if the number is a multiple of 3.
* Print the `number` followed by the string "Buzz" if the number is a multiple of 5.
* Print the `number` followed by the string "FizzBuzz" if the number is a multiple of both 3 and 5.
* Print the `number` if none of the above is true.

A solution could look like this:

<script src="https://jsfiddle.net/lthr/ovjq55a7/embed/css,js,result/"></script>

The above solution might be sufficient as a simple draft, but there are a number of problems.
One of them being that of mixing up the output with the logic for determining what to print,
there's no seperation of concerns.

## Seperation of concerns


<script src="https://jsfiddle.net/lthr/x61rj9yk/embed/js,result/"></script>

Now `test()` is a pure function, and both `formatOutput()` and `print()` can be maintained 
independently of the other parts.
