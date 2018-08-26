# Learning Python with Turtle

## How to start

In your web browser go to https://trinket.io/turtle.

## Import the Turtle module

A **module** is an independent part that can be put together with other modules to make a more complicated thing. For example, you could bricks, doors and windows modules that you can put together in different ways to make a house.

It is similar in programming. In Python, modules are independent pieces of code that you can combine together in many different ways to build something more complicated.

You can write your own Python modules just by making new Python files. In Trinket you are given a module to start with called `main.py`, but you can add more by clicking on the **+** button.

Lots of people have written Python modules that you can use in your own programs. This saves you time because you don't have to write everything yourself. Trinket has a few of these that you can use and you can see a list of them all if you click on the **?** button.

**Turtle** is one of the modules that Trinket has. This module has code for moving a turtle around the screen. The turtle holds a pen, so it draws a line whenever it moves.

To get started we need to tell Python that we want to use the Turtle module in your own program. To do this we need to write one of the **keywords** that are special to Python to tell it to do something. To tell Python to use another module in your program you write the `import` keyword as follows:

`import turtle`

## Making a Turtle

Now that we have imported the `turtle` module, the next thing we need to do is to use the code in that module to make a turtle that we can use for drawing. We can make one turtle and give it instructions so it draws a picture, or we can make two turtles and give them both instructions, or as many as we like.

First let's learn about **functions**. A **function** is a small piece of reusable code inside a Python module. To use a function we must **call** it. Think of this a bit like a short telephone call where we call it up, ask it a question and it gives us an answer, then we hang up. When we call a function in Python, we put the details of the question - we call these details the  **arguments** - inside brackets called parentheses `(` and `)`.

To make a turtle we use a function called `Turtle` in the `turtle` module that we imported. All this function does is make a new turtle for us to use, so we don't need any arguments (the details of the question in the telephone call) and so we don't need to put anything between the `(` and `)`. Here is how we call the `Turtle` function in the `turtle` module with no arguments:

`turtle.Turtle()`

The answer from calling this `Turtle()` function is a new turtle **object**. Almost there, however to be able to use this turtle object for drawing we need to give it a name!

In Python a name can be any word using letters, numbers or underscores (_), but it cannot start with a number. Here are some examples of names we could choose:

`alice`, `Tilsbury12`, `green_turtle`, `_turt13`

In Python, names are usually chosen so they are all lower case (no capital letters), and words are separated by underscores, for example `my_blue_turtle`.

Let's call our first turtle object `trevor`. To make a turtle object with this name we write:

`trevor = turtle.Turtle()`

The `=` (equals) symbol here means **be given the value of** or **be assigned the value of**. So the thing that comes before the equals symbol is given the value of the thing that comes after it. So here we are telling Python to make something called `trevor` be given the value of calling the `Turtle()` function in the `turtle` module with no arguments. Remember the answer from calling the `Turtle()` function was a new turtle object? So now we have made a new turtle object and given it the name `trevor`!

Type in the following program in to Trinket then press the play **>** button to **run** the code:

```
import turtle
arthur = turtle.Turtle()
arthur.forward(100)
```

You should see a line is drawn on the screen.

## Variables

In programming, a **variable** is a named thing whose value can change. A **constant** is a named thing whose value cannot change.

`10` is a constant. This is just the number ten. It is always the number 10 and never changes.

`trevor` is a variable. We made up the name and we used the = symbol to give it the value that was returned when we called the `turtle.Turtle()` function. The value of `trevor` can change however. On the next line of our program we could say `trevor = 10` to give it the value ten instead.

Variables are very useful when we want to do some maths. Here we create a variable called `arthur` and give it the value eleven.

`arthur = 11`

Now we can change the value of the variable called `arthur` to be one more than its current value:

`arthur = arthur + 1`

After this line of code `arthur` would have the value twelve.

You can see what value a variable has by calling the Python `print()` function. Try it out by deleting any code already in Trinket, then typing the following code in to Trinket then pressing the play button to **run** the code:

```
arthur = 11
print(arthur)
arthur = arthur + 2
print(arthur)
```

The output will be shown in the panel at the bottom right of the Trinket screen. Notice how we passed an **argument** to the `print()` function with the variable name whose value we wanted to output.

We can use the plus operator (+) for addition, the minus operator (-) for subtraction, the star operator (*) for multiplication, and the forward slash operator (/) for division. Sometimes it is not clear which order these operations happen, so we can use parentheses ( and ) again to make it clear. For example:

`arthur = (arthur * 2) - (5 - 2)`

If `arthur` was 12 before this line of code then it would have the value 21 afterwards. The parentheses group together the maths operations so we end up subtracting 3 from 24. Can you try it using Trinket and the `print()` function?

## Types of values

As we have seen, named variables in Python hold values. Values can be different types. 

We have seen variables holding a value that is an object  (a turtle), and holding values that are numbers.

Variables can also hold values that are words or sentences or any other sequence of **characters** - the letters, numbers and other symbols you can type on a computer keyboard. A value that is a sequence of characters is called **text** or a **string of characters** or just a **string** for short. To create a string value in Python you use quotes (') or double quotes (") at each end of the sequence, for example:

`arthur = "this is a string"`

`moss = 'My kitten is 5 weeks old.'`

We can join strings together using the + operator, and display their value using the `print()` function, for example:

```
arthur = 6
print("Arthur is " + arthur + " years old")
```

Try it by writing the code in Trinket and cliking on the play button to **run** your program!

Later on we will see other types of values but for now we can do a lot with numbers, strings and turtle objects.

## Turtle functions

We have seen two functions already:

1. The `Turtle()` function in the `turtle` module, called by writing `turtle.Turtle()` that returns a new turtle object.
2. The `print()` function built in to Python, that we pass an argument to and it displays the value on the screen.

A turtle object also has functions. To call a function on a turtle object we use a dot `.` and the name of the function. For example, if we have a turtle object in a variable named `arthur` then we can call the `forward()` function passing a distance of 100 as the argument by writing `arthur.forward(100)`.

The turtle object has other functions for movement:

* `backward(distance)` moves the turtle backwards the given distance
* `left(angle)` makes the turtle turn to the left the given angle. The angle is in degrees, so passing a value of 90 as the argument turns a right-angle to the left.
* `right(angle)` makes the turtle turn to the right the given angle.

The turtle starts at location (0, 0). The first number is the horizontal distance from the centre of the screen. The second number is the vertical distance from the centre of the screen. The turtle starts pointing to the right, so after running `forward(100)` the new position is (100, 0).

Try the following program to draw a square:

```
import turtle
arthur = turtle.Turtle()
arthur.forward(100)
arthur.right(90)
arthur.forward(100)
arthur.right(90)
arthur.forward(100)
arthur.right(90)
arthur.forward(100)
arthur.right(90)
```

You can move a turtle to a specific position using the `goto(x, y)` function. You can move a turtle back to the centre of the screen using the `home()` function.

The turtle holds a pen and draws a line every time the turtle moves. You can stop drawing using the `penup()` function and start drawing again using the `pendown()` function. Use `pencolor(color)` to change the colour of the pen, for example `arthur.pencolor("red")`. 

Can you change the square program to draw a blue square?

The `write(text)` function will make the turtle write words (a string value), for example `arthur.write("hello")`. 

## Making your own functions

Functions are small pieces of reusable code. We have used several functions including `print()`, `forward()` and `pencolor()`. We can write our own functions so we can run the same piece of code again and again.

To write a function we use the `def` keyword to **define** a new function. When we define a new function we give it a name and also list the names of any arguments we want the function to have.

Let's make a function that will be passed a turtle and will use it to draw a square of a given size. We start by writing:

```
def square(t, size):
```

Notice how the line of code ends with a colon `:`. In Python, when a line ends with a colon it means it is the beginning of a block of code. Blocks of code must be **indented** which means each line must start with the same number of spaces. We will type two spaces at the beginning of each line in a block, so our function looks like this:

```
def square(t, size):
  t.forward(size)
  t.right(90)
  t.forward(size)
  t.right(90)
  t.forward(size)
  t.right(90)
  t.forward(size)
  t.right(90)
```

We can now use this function to draw as many squares of different sizes as we like, moving the turtle and changing its colour between each call to our `square()` function.

Type in the following program to try the function:

```
import turtle

def square(t, size):
  t.forward(size)
  t.right(90)
  t.forward(size)
  t.right(90)
  t.forward(size)
  t.right(90)
  t.forward(size)
  t.right(90)

arthur = turtle.Turtle()
square(arthur, 50)
arthur.right(45)
arthur.pencolor("red")
square(arthur, 20)
```

## Repeating using loops

Our `square()` function repeats four the same two lines to move the turtle forward and turn right 90 degrees. Instead of copying the same code like this we can use a **loop** to run the same code a number of times.

Here is another way to write the `square()` function in Python using a **loop**:

```
def square(t, size):
  for i in range(4):
    t.forward(size)
    t.right(90)
```

We are using two new Python keywords here, `for` and `in`, and a new function `range(length)`. 

The `range()` function returns a **list** of numbers with the given length, counting up from zero, so `range(4)` gives us the list of numbers [0, 1, 2, 3].

The line `for i in range(4):` tells Python to repeat the code in the **block** that follows, one time for each item in the list, setting the variable `i` to be the item in the list. Remember that a colon `:` means we are starting a new block and blocks must be indented? We were already inside the `def square(t, size):` block so we had to indent another level inside the `for` loop.

Try the following loop in Trinket. Before you run it, what numbers do you think it will print?

```
for i in range(10):
  print(i)
```

Now we have made our `square()` function simpler using a loop, we can also use a loop to call our `square()` function several times. Try the following program to draw a pattern with squares:

```
import turtle

def square(t, size):
  for i in range(4):
    t.forward(size)
    t.right(90)

arthur = turtle.Turtle()
for i in range(8):
  square(arthur, 100)
  arthur.right(45)
```

## Drawing speed

You can make drawing faster using the turtle `speed()`, `tracer()` and `update()` functions.

* `arthur.speed(number)` sets the speed of animating drawing each line, where passing 1 is the slowest and 10 is the fastest. If you pass the special value 0 then it is even faster as no animation takes place.

* `arthur.tracer(number)` sets the number of animation steps to draw before updating the screen, so `arthur.tracer(10)` will only update the screen every tenth animation step. 

* To force updating the screen use the `update()` function.

Using a combination of these makes drawing much faster.

```
import turtle
arthur = turtle.Turtle()
arthur.speed(0) # no animation so each line is one step
arthur.tracer(4) # update the screen every fourth line

... some complicated drawing ...

arthur.update() # make sure the last few lines appear on the screen
```

Here is another new feature of Python. Any line starting with a hash symbol `#`, or everything on a line following `#` is treated by Python as a comment and is ignored. 

## More shapes

Now we have a `square()` function, can you write some others?

Before we start, let's make a new Python **module** to keep all our helpful functions. Click on the + button in Trinket and give the new file the name `shapes.py`. Move the `square()` function to the our new `shapes` module then in `main.py` try the following code:

```
import turtle
import shapes

arthur = turtle.Turtle()
shapes.square(arthur, 100)
```

* Write a `triangle()` function in the `shapes` module that has arguments of a turtle and a size. Draw a pattern using your new function and the `square()` function by writing a new program in the `main.py` file.

* Write a `hexagon()` function that has arguments of a turtle and a size. Add some hexagons to your pattern.

* Can you write a `polygon()` function that has arguments of a turtle, number of sides, and a size?

* Can you draw a shape that looks like a circle using your `polygon()` function? In the future you can also use the turtle object's own `circle()` function to do this, for example `arthur.circle(50)`.

* How would you write a `rectangle()` function that took arguments of a turtle, a long size and a short size? What loop would you use inside the function?

* Write a function `window()` that takes a turtle and a size and draws a window made of a large square and four smaller squares inside. Call your `square()` function from inside your `window()` function and remember to use `penup()` and `pendown()` to move the turtle without drawing a line.

* Write a function `door()` and finally a function `house()` that draws the outline of a house shape and uses your `door()` and `window()` functions. Can you use a loop to draw a repeating pattern of houses?

We can make a spiral with a loop, turning the same angle each time but drawing a slightly longer line on each step. To do this we need to use some maths to change the value of a variable each time we go round the loop. Type in and run the following program:

```
import turtle
arthur = turtle.Turtle()
size = 1
for i in range(50):
  arthur.forward(size)
  arthur.right(90)
  size = size + 5
```

* Turn the spiral program in to a `spiral()` function that has arguments `loops` (for the number times to run the loop), `angle` for the angle to turn each time, and `step` for the amount to add to size each time around the loop. 

* Write programs to try running your spiral function passing different values for the arguments to experiment with how they change the spiral that is drawn. Remember you can change the drawing speed.

Here is a function that takes as an argument another function.

```
def square_of_shape(t, func, size):
  for i in range(4):
    func(t, size)
    t.penup()
    t.forward(size)
    t.right(90)
    t.pendown()
```

Add the new function to your `shapes` module then try calling it:

```
import turtle
import shapes

arthur = turtle.Turtle()
shapes.square_of_shape(t, shapes.triangle, 100)
```

Look carefully. When we wrote `shapes.triangle` we did not write any parentheses `()`. This is because we didn't want to **call** the triangle function immediately, instead we wanted to pass its **definition** to the `square_of_shape()` function.

* Can you write a `spiral_of_shape()` function? What arguments do you want it to take? Can you use your new function to draw a spiral of houses?

## Drawing ideas

You can colour-in, or **fill**, shapes using the turtle's `fillcolor()`, `begin_fill()` and `end_fill()` functions. For example, the try the following program to draw a hexagon with a blue outline and filled in red.

```
import turtle
import shapes
arthur = turtle.Turtle()
arthur.color("blue")
arthur.fillcolor("red")
arthur.begin_fill()
shapes.hexagon(arthur, 50)
arthur.end_fill()
```

* Change the functions you wrote earlier to fill in the door, windows and background of the house different colours.

* Make an `arc()` function that draws part of a circle, then a `petal()` function using two arcs, a `flower()` function that draws a green stem and leaf using the `arc()` and `petal()` functions and uses a loop to draw a pattern of petals filled with a given colour. Use your `flower()` function to draw a field of flowers or a flower garden outside a house using the `house()` function you wrote before.

* Draw a spider web using rings of arcs or a spiral of arcs and lines going our from the centre.

* Write a `car()` function that draws a car.

## Returning values from functions

Python has a module called `random` with functions that return a different answer each time they are called.

```
import random

# prints a random number between 3 and 12 inclusive
print(random.randint(3, 12))

# prints a string value from the list
print(random.choice(["red", "blue", "green"]))
```

Here is a new type of value in Python, a **list**. You create list values using the square bracket symbols `[` and `]`. For example, make a list of numbers with `[0, 1, 2, 3]` or strings with `["arthur", "moss"]`. 

Think back to when we first wrote a loop with `for i in range(4):`. Here the `range(4)` function returns a list `[0, 1, 2, 3]`. In the same way we can write a loop `for i in [0, 4, 12]:` that sets `i` to each number in turn, or `for i in ["red", "blue", "green"]:` that sets `i` to each string value in turn. Don't forget the colon on the end of the line!

As well as looping over lists, we can use the `choice()` function in the `random` module to pick an item from a list, so `random.choice(["red", "blue", "green"])` will give us a random colour name.

Add to your `shapes` module:

```
import random

colors = ["red", "blue", "yellow"]

def pick_color():
  return random.choice(colors)
```

This new function uses the Python `return` keyword to make our function pass back an answer - the randomly chosen colour name.

We can use this function with, for example `print(shapes.pick_color())` or `arthur.fillcolor(shapes.pick_color())`.

* Can you use your `flower()` function from earlier and the `pick_color()` function to draw flowers with random colours?

* Can you use the `random.randint()` function and the turtle's `move(x, y)` function to draw random coloured flowers at random locations on the screen?

## Writing games...

* Change the shape and size of the turtle

* Add a background

* Controlling with the keyboard

* Remembering the state of the game

* Showing the score


