# Problem Set 1: Mario in Python

# Introduction
We'll step into Python by reacreating our first C problem set: [Mario](http://cdn.cs50.net/2015/spring/psets/1/pset1/pset1.html#itsa_mario). The focus here is learning a new way to write code for a problem that we already understand. You might find it useful to scan your solution in C just to orient yourself.

# Getting ready
Open a Terminal window and use Homebrew to install python 3.4: `brew install python3`. 

Next, install [PyCharm](https://www.jetbrains.com/pycharm/). The Community Edition will be fine for our purposes, but if have a `.edu` email then you can get a free copy of the Professional Edition. 

Then, fork this repo and fire up PyCharm. In the welcome dialog, select Configure > Preferences and search for github in the search box. That'll bring up the GitHub config settings so you can connect your account to PyCharm. Apply the settings and close out the preferences dialog, and select Check Out From Version Control > GitHub from the welcome dialog. Choose your new fork, and your new project workspace should load after a few seconds.

# Getting started
We'll follow the original pset spec pretty closely. In the `pset1` folder of your project, create a new file, `mario.py`. You'll need to `import sys` at the top, so do that first. Then stub out a `main` function and the code to run it:
```python
import sys

def main(argv):
	print("Hello, Mario!")
	
if __name__ == "__main__":
	main(sys.argv)
```
That last block will cause the script to run your `main` function when the script loads. `sys.argv` is analagous to `argv` in C, and is a list of the arguments passed to the program at the command line. The `print` is there just so we can do a test run of our code before diving in too far. Let's do that now.

Open the Terminal panel in PyCharm (click on the square icon at the bottom left, if you don't see the Terminal panel button at the bottom of your window), and `cd pset`. Then run your file: `python mario.py`. You should see your message printed out.

# What to do
Write a program that accepts a single integer as a command line (CL) argument and prints out a pyramid consisting of `#` characters and spaces at the command line. Your program should:
* Print out a usage message if no CL arguments are passed, and then quit
* Attempt to cast the first CL argument to an integer using `int()`. If this fails, Python will raise a `ValueError` exception, so you'll need to wrap this line of code in a `try/except` block. If such an exception is raised, your program should print out an informative message and quit.
* Validate that the integer input is between 0 and 23. If it isn't, `raise` a `ValueError` of your own, being sure to include a helpful message.
* Once you know that you have valid input, implement the code to draw your pyramid. You'll need to make use of `for` loops, the `range` function, and `sys.stdout.write()`
* When you're done, commit and push your code up to GitHub, and send me a note via email. Then proceed to pset2.

# Resources
* [Python 3.4.3 language reference](https://docs.python.org/3/reference/), including:
	* [`if` statement](https://docs.python.org/3/reference/compound_stmts.html#the-if-statement)
	* [`for` loop](https://docs.python.org/3/reference/compound_stmts.html#the-for-statement)
* [Errors and exceptions in Python](https://docs.python.org/3.4/tutorial/errors.html) (includes info on `try/raise` blocks)
* [Built-in functions](https://docs.python.org/3/library/functions.html), including:
	* [`int()`](https://docs.python.org/3/library/functions.html#int)
	* [`range()`](https://docs.python.org/3/library/functions.html#func-range)
