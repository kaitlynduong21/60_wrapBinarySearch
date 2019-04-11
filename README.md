# implement List.indexOf

`while`-style and recursive implementations at the top of
OrderedList_inArraySlots.java

[Java API on the `indexOf` method](https://docs.oracle.com/javase/10/docs/api/java/util/List.html#indexOf(java.lang.Object))

based on [solutionsHolmes/5D_genericTypes/OrderedList_inArraySlots_v2/](https://github.com/stuyvesant-cs/solutionsHolmes/tree/master/5D_genericTypes/OrderedList_inArraySlots_v2)
as of 2019-04-10 04:48

0. What is meant by y = log2x ? Express its meaning in a .

  A log function is the inverse function of an exponential function. x is equal to the power that you raise 2 to in order to      get the value y.

1. What does its graph look like?


## recursive solution

0. The Problem
  Return the index of the first instance of a given value in an ordered list using binary search.
1. State the recursive abstraction
  
2. Identify the parts of this solution that correspond to the six parts of a generalized recursive solution.

  Problem: return the index of the first instance of a given value
  
  Recursive Abstraction: 
    When asked to find the index of a given value, the recursive abstraction can compare the given value to the value on the page that is halfway between the low and high limits.
    
  Solutions to the base cases: 
  
    if (low > high) return -2; 
    if (integerInSlot == findMe) return index;
    
  Solution(s) to recursive cases:
  
    if (integerInSlot < findMe) return indexOf_recursive( findMe, low, pageToCheck -1)
    if (integerInSlot > findMe) return indexOf_recursive( findMe, pageToCheck + 1, high)
  
  
