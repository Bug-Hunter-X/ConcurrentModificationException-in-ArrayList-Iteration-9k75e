# ConcurrentModificationException Example in Java
This repository demonstrates a common error in Java involving the ConcurrentModificationException when iterating and modifying an ArrayList.  The example shows the problematic code and the solution.

## Problem
The provided Java code attempts to remove even numbers from an ArrayList while iterating over it using an enhanced for loop. This approach leads to a ConcurrentModificationException because the iterator's internal state becomes invalid when the list is modified.

## Solution
The solution demonstrates two safe approaches to avoid the ConcurrentModificationException:

1. Using an Iterator: The code iterates using an Iterator and removes elements using the Iterator's remove method.
2. Using an iterator and removing elements in reverse order: This technique avoids issues by removing items starting at the end of the list, thus maintaining iterator validity. 

This example highlights the importance of understanding the limitations of modifying a collection while iterating directly.
