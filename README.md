# plus
For all your adding needs, up to numbers of about 450 because otherwise the maximum recursion depth is exceeded.

## Installing

The package can be installed using `pip install pluspy`.

## Example

To get the sum of two **positive integers** `a` and `b`, you would use `plus(a, b)`:

```
>>> from plus import plus

>>> plus(2, 5)
7
```

Keep in mind the module is called `plus`, _not_ `pluspy`.

## FAQ

### What is plus?
Plus was made to redefine the '+'operator in a recursive way, without using the '+'-operator itself.

### Why?
This library was inspired by the enormous amount of `isEven` and `isOdd`-type memes, including one where '+' was defined by hardcoding every possible combination of the first 100-or-so numbers.

It was not made with the intention of being used (obv.), but rather to see how ridiculous I could make this.

The last 5 lines (`while`-loop & `bitshift`) by themselves are actually enough to add two numbers together (and it doesn't exceed the maximum recursion depth instantly), which was also done for this very reason. That part being in there adds to the overall idea.

### Why is there a cache?
Well you see, when using numbers above 10 it started to get a bit slow. Calculating `plus(50, 20)` had been running for half an hour, and wasn't showing any signs of stopping any time soon.

This meant I had to introduce `dynamic programming` to speed it up a bit, and store results of calculations that had been made before.