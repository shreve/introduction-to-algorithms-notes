## Chapter 1. Foundations

### Definitions

**Algorithm**
> A defined procedure, or list of computational steps, that takes 0 or more
> inputs and produces 1 or more outputs. It can be defined in English, a
> programming language, or even as a hardcoded circuit as long as it's a
> complete set of instructions.

**Correct**
> An algorithm is correct if for every input, it returns the correct output.

### 1.1 Algorithms

An algorithm is a tool to solve a defined problem.

A problem should be well-defined enough that it encapulates all cases, meaning
that it should accommodate it's inputs and outputs as variables.

Problem: sort <a1, a2, a3, ..., an> such that a1 < a2 < a3 < an

Instance of a problem: sort <3, 5, 1, 6, 2, 9> in increasing order

There are many types of algorithms for a given problem, and the best one depends
on the constraints of the instance of the problem you're trying to solve.

#### NP-Complete Problems

There is a subsection of problems classified as NP-complete. These problems are
interesting because:

1. No one has found an efficient algorithm to solve them
2. No one has proved that an efficient algorithm to solve them can't exist
3. If a solution for 1 is found, it can be applied to all
4. If you can identify a problem as NP-complete, you likely can't find the
   _best_ solution, so you can skip to finding good enough.

The best known example of NP-complete is "The traveling salesman problem", where
the desired output is the most efficient route to traverse that yields the
lowest overall distance, yet hits all desired stops.

#### Exercises

**1.1-1** Give a real-world example that requires sorting or a real-world
example that requires computing a convex hull.

> Most technology applications require sorting some sort of list. One of the
> most prevalent is ecommerce applications sorting products by all sorts of
> indicators.
>
> A problem that requires computing a convex hull is collision detection in
> video game engines. When two hulls intersect, a collision has occurred.

**1.1-2** Other than speed, what other measures of efficienct might one use in a
real-world setting?

> Energy use, memory use, bandwidth use (if transmitting data) may all be used
> to compare the relative efficiency of an algorithm.

**1.1-3** Select a data structure that you have seen previously, and discuss
its strengths and limitations.

> I particularly like structs because they are friendly for programmers. They
> package up data nice and neatly with labels for each piece. However, structs
> are less effective because the CPU needs to deal with the extra structure
> over, say, an array instead.

**1.1-4** How are the shortest-path and traveling salesman problems given above
similar? How are they different?

> The problems are similar in that the correct output is a route that is the
> shortest possible path to traverse the problem map.
> They are different in that the shortest path problem has an input of two
> unique input points, and the output is the path from one to the other. The
> traveling salesman problem inputs a list of many points that must each be
> reached before returning to the original.

**1.1-5** Come up with a real world problem in which only the best solution will
do. Then come up with one in which a solution that is "approximately" the best
is good enough.


> The algorithm used to compute the amount of anesthesia a patient should be
> treated with for a given surgery must be absolutely correct. Too much, and the
> patient could die. Not enough, and they'll wake up mid-surgery, and
> potentially cause complications.
> The algorithm used to calculate the remaining gasoline in a car's tank doesn't
> require the same amount of accuracy. For example, my car fluctuates this value
> quite often, and it stops calculating when the value is below 45 miles, yet
> I've never been stranded.
