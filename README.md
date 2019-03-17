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
You are already familiar with the opposite of declarative programming: imperative programming.
In imperative programming you have statements. 

'''
int main()
{
  int n, first = 0, second = 1, next, c;
 
  printf("Enter the number of terms\n");
  scanf("%d", &n);
 
  printf("First %d terms of Fibonacci series are:\n", n);
 
  for (c = 0; c < n; c++)
  {
    if (c <= 1)
      next = c;
    else
    {
      next = first + second;
      first = second;
      second = next;
    }
    printf("%d\n", next);
  }
 
  return 0;
}
'''
