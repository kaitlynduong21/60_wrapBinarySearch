# implement List.indexOf

`while`-style and recursive implementations at the top of
OrderedList_inArraySlots.java

[Java API on the `indexOf` method](https://docs.oracle.com/javase/10/docs/api/java/util/List.html#indexOf(java.lang.Object))

based on [solutionsHolmes/5D_genericTypes/OrderedList_inArraySlots_v2/](https://github.com/stuyvesant-cs/solutionsHolmes/tree/master/5D_genericTypes/OrderedList_inArraySlots_v2)
as of 2019-04-10 04:48

## recall inverse functions and logarithms

**0. What is meant by y = log2x ?**

  A log function is the inverse function of an exponential function. x is equal to the power that you raise 2 to in order to      get the value y.

**1. What does its graph look like?**
  
  The graph of log2x is the log of 2^x reflected along the line y = x. It has a vertical asymptote at y = 0 as x can never be negative and it has a horizontal asymptote. The graph is an increasing function but increases at a decreasing rate. As x gets larger, the graph flattens out and the rate of change decreases.

## recursive solution

**0. The Problem**

  Return the index of the first instance of a given value in an ordered list using binary search.
  
**1. State the recursive abstraction**

  When asked to find the index of a given value, the recursive abstraction can find the given value in a list half the size of the previous list (in the first loop, the original list).
  
**2. Identify the parts of this solution that correspond to the six parts of a generalized recomparecursive solution.**

  Problem: return the index of the first instance of a given value
  
  Decision between base cases and recursive cases:
    Base Cases: 
    
    if (low > high) //base case 0
    if (comparison == 0) //base case 1
    
  Solutions to the base cases: 
  
    return -2; //solution to base case 0
    return index; //solution to base case 1

    
  Recursive Abstraction: 
    Find the given value in a list half the size of the previous list (in the first loop, the original list).
    
  Solution(s) to recursive cases:
  
    if (comparison < 0) return indexOf_recursive( findMe, low, pageToCheck -1)
    if (comparison > 0) return indexOf_recursive( findMe, pageToCheck + 1, high)
    
   No leftover procession or combination.
    
  
  
