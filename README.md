# Functional-Programming-made-easy
This repo is here to provide an introduction to different functional programming concepts. The intention is to show how easy (and practical) functional programming (FP) can be. Since there are many advantages on FP, this should also be a motivation to start learning FP. Many programmers start with imperative programming and then go on with object oriented programming, therefore I will also compare some concepts to show the advantages.
Feel free to contribute!

# Why should I learn functional programming?
Currently functional programming is quite hyped. Most languages implement more and more functional concepts in each version. One reason for it: [Moore's Law](https://en.wikipedia.org/wiki/Moore%27s_law). In past, processors got faster and faster until a few years ago we reached some physical borders. Then processors suddenly got more and more cores. And if that is not enough some programs are running even on multiple servers. Here comes functional programming in play. One big advantage of FP is that it is much easier to write concurrent programs.

## Who should read this?
All who want to learn something about functional programming! This course is intended to be build on your existing knowledge and guide you to the core concepts of functional programming.

## Prerequisites
I assume that you have already have basic understanding in some programming language. You should be familiar with imperative and some OOP principles.

## Examples
Examples are provided in C# and/or F#. If I find the time I will also add examples in Scala and Haskell. Generally the language doesnt matter to show the principles. However in the beginning its easier to have examples in a familiar language.

## Outline

### 01 - Basics 
#### What is FP
Functional programming is a programming paradigm. Rather than how something is done, you specify what needs to be done (also called declarative programming). At first this sounds quite strange, but I am sure you will be familiar with it quite soon.
You are already familiar with the opposite of declarative programming: imperative programming. But I am sure, you already cam across some functional concepts. I will show you an example. 
We have a list of numbers

```
 IList<int> numbers = new List<int>() { 0, 3, 6, 21, 35, 4 };
 
```
Now we want to add 5 to each number. In the typical iterative way we would write something like this:

```
public List<int> imperativeAdd5(List<int> numbers)
{
    List<int> resultList = new List<int>();
            
    foreach (int number in numbers)
    {
        int numPlus5 = number + 5;
        resultList.Add(number);
    }

    return resultList;
}

```
Here we tell the compiler excactly how he should add 5 to each number. We tell him that he has to create a new list to store the results, then he should take the first number add 5 to it, add the result to the result list. Then go to the next number... and finally return the list!
So how does this code look in functional programming?

```
public List<int> functionalAdd5(List<int> numbers)
{
    return numbers.Select(x => x + 5).ToList();    
}

```
As I mentioned earlier, we don't care here how 5 is added. Technically in the background it is done with a loop, however this is not something we want to know here. So we straightforward can select the numbers in the list and add 5 to them.
So as you can see functional programming doesnt require any wizard skills, it is straightforward!
