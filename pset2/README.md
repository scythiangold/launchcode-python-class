# Problem Set 2 - Mario with a class
Now that we have some basics of Python under our belt, let's start working with objects.

## Goals
At the end of the exercise, you should be able to:

* Create a class in Python
* Use methods and properties within a class
* Explain why classes are useful
* Explain the concept of encapsulation, and how class creation embodies this concept

## Getting ready

## What to do
Start by copying your Mario.py file into the `pset2` directory.

* Create a Pyrmaid class below your `main` function, and encapsulate the pyramid creation and drawing logic into that class. Your class should have a constructor, a `height` property that is set in the constructor, along with a `draw` method to output the pyramid.
* Have your `main` function create a Pyramid instance after validating input, and then call `.draw()` on that instance
* Refactor your code to accept an optional second command-line argument, that should represent a file name that our program can optionally print to.
* Refactor the Pyramid class so that it's constructor takes a file name parameter. You can deal with the optional part of this requirment in any number of ways. Maybe if an empty filename (i.e. `''`) is passed then it prints to the screen (aka standard out or stdout). Or perhaps you provide a default value of `None` for the file name paremeter and check that in your constructor or `draw` method. (The former may be easier, but be sure to [read up on default parameters](http://docs.python-guide.org/en/latest/writing/gotchas/) if you think you want to tackle the latter.)

## Resources
There are mulitple, overlapping resources here. Give each a scan, and use whichever is most beneficial. The "Learning to Speak Object Oriented" link is highly recommended for reinforcing new language and ideas around these concepts.

### Classes and objects in Python
* [Encapsulation (Wikipedia)](http://en.wikipedia.org/wiki/Encapsulation_(object-oriented_programming))
* [An Introduction to Classes and Inheritance in Python](http://www.jesshamrick.com/2011/05/18/an-introduction-to-classes-and-inheritance-in-python/) - note that the section on inheritance/sublcasses is not necessary for this problem set
* [Object Oriented Programming in Python](http://anandology.com/python-practice-book/object_oriented_programming.html)
* [Modules, Classes, and Objects](http://learnpythonthehardway.org/book/ex40.html)
* [Learning to Speak Object Oriented](http://learnpythonthehardway.org/book/ex41.html)