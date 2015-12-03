# Introduction to Looping

## Abstraction and Repetition in Programming

As programmers, we are lazy. This isn't a bad thing. It means we strive for efficiency in every way. If we can get our program to behave in a certain way or carry out a certain task with fewer lines of code, we do it. We think of our code like an artist thinks of their paintings or an architect thinks of their buildings. We want the programs we write to be beautiful. That means they should be simple and eloquent. 

What does it mean to write code that is both efficient and eloquent? It means we rely on abstraction. A method is a form of abstraction. 

For example, let's say we have a program that we want to greet a given user. We could do so with the following code:

```ruby
puts "Hello, program user."
``` 

This code is literal. It greets some un-identified user with the title `"program user"`. 

In order to greet someone else later on, we would have to re-write the above code, changing the title of the person we are greeting:

```ruby
puts "Hello, someone else."
```

Not only do we have to repeat the same line of code again and again, changing one consistent thing about it each time, but the use of the line of code above isn't descriptive of the job we are trying to accomplish. 

This line of code has a responsibility, it's responsibility is to greet the user. But in order to understand that, you have to read the text that we are `puts`-ing out and really think about it. 

We can make this code eloquent, i.e. expressive of the job it is trying to accomplish, and re-usable and flexible by wrapping it in a method that takes an argument:

```ruby
def greet_user(name)
  puts "Hello, #{name}"
end
```

Now we have a method name that expresses the job or responsibility of the code it contains *and* we have a way to re-use the same bit of code again and again, throughout our program, simply by calling the method. 

Repetition and abstraction in programming go hand-in-hand. It's hard to imagine a program that must carry out a certain responsibilty or do a certain job *only once*.

You might be writing code for a game that must ask the user for input again and again, until they either win or lose. You might need to send a user of a web application updates about their account repeatedly. You might need to do something as simple as `puts` out some text to the terminal a specified number of times. 

All of these scenarios, and many more, can be accomplished with a programming construct called **looping**. 

## Looping

Imagine a scenario in which we are writing a program that needs to `puts` out a greeting to the user a certain number of times, let's say ten times. 

We might accomplish it like this:

```ruby
puts "Hi! Welcome to my very repetitive program"
puts "Hi! Welcome to my very repetitive program"
puts "Hi! Welcome to my very repetitive program"
puts "Hi! Welcome to my very repetitive program"
puts "Hi! Welcome to my very repetitive program"
puts "Hi! Welcome to my very repetitive program."
puts "Hi! Welcome to my very repetitive program"
puts "Hi! Welcome to my very repetitive program"
puts "Hi! Welcome to my very repetitive program"
puts "Hi! Welcome to my very repetitive program"
puts "Hi! Welcome to my very repetitive program"
``` 

This implementation has a couple of obvious drawbacks. First, I had to manually type that line of code ten times, which goes against my lazy programmer nature. Secondly, are you sure I typed it ten times? Go ahead and count, I'll wait. 

It's there eleven times! Another drawback: you need to very closely examine each line to make sure they are in fact identical. In fact, there is a discrepancy in the set of lines above. Can you spot it?

Code like the snippet above is hard to maintain, but, above all, it is not eloquent. It doesn't immediately convey the task it is responsible for carrying out to the person reading it. 

**Loops**, however, allow us to tell our program to do the same thing over and over with just a few simple, clear, and easy to understand lines. 

There are a number of different looping constructs available to us. In other words, there are a few different types of looping methods and implementation that we will learn. The basic principle, though, is that looping allows us to **abstract** away the actual mechanics of enacting the same, or similar, lines of code a certain number of times. Instead of explicitly telling our program to `puts` out a phrase ten times, we can use a loop like this one:

```ruby
10.times do 
	puts "Hi! Welcome to my very repetitive program"
end
```

Copy and paste the above code snippet into your terminal and hit `enter`. You should see:

```bash
Hi! Welcome to my very repetitive program
Hi! Welcome to my very repetitive program
Hi! Welcome to my very repetitive program
Hi! Welcome to my very repetitive program
Hi! Welcome to my very repetitive program
Hi! Welcome to my very repetitive program
Hi! Welcome to my very repetitive program
Hi! Welcome to my very repetitive program
Hi! Welcome to my very repetitive program
Hi! Welcome to my very repetitive program
 => 10 
```

Regardless of whether we understand how the code above works, we can see the advantages it has over our first implementation. First, we are able to achieve the same result as our first implementation with far fewer lines of code. Secondly, it eliminates the room for error that manually typing out `puts "Hi! Welcome to my very repetitive program"` allows. 

Lastly, it clearly conveys to the reader exactly what it will accomplish. It reads like this "ten times do `puts` out this phrase to the terminal". This is abstract, rather than the explicit typing of ten lines of identical code, which is literal. And this is eloquent, because it speaks for itself. 
