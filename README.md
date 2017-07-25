# Interview Quiz

## Quick Recap

### Big O

Big O is the language and metric we use to describe the efficiency of algorithms. In theory, big O means the upper bound limit, but for practical purposes we'll use the tightest/closer upper bound possible (basically what academics call big theta). For example, iterating over all elements of an array should be described as O(n), although in theory O(n^2), O(n^3) are also valid upper limits.

Remember that O(1) < O(log n) < O(n) < O(n * log n) < O(n^2).

Also remember to drop constants, basically O(2 * n) could simply be described as O(n).

**Time complexity** is the asymptotic runtime of an algorithm. It's how fast it runs. For example, iterating over an array is O(n).

**Space complexity** is the asymptotic amount of memory used by an algorithm. It's how much memory it takes.

## Quiz 1 - Array

Edit this markdown by replacing the `> EDIT ME`s below with your answers.

### Find key

Given an array `A` of alpha characters `[A-Za-z]`, create a function that returns the first index at which a given element can be found in the array, or `-1` if it is not present.

**Example of `A`**

| i    | 0    | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | 10   |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| A[i] | G    | d    | e    | Z    | e    | k    | I    | X    | d    | S    | e    |

**Solution**

```
function getFirstIndex(element){
  return A.indexOf(element);
}
```

**Time and space complexities**

> EDIT ME

### Are values unique?

Create another function to identify whether `A` has unique elements.

**Solution**

```
function hasDuplicates(array) {
    var valuesSoFar = Object.create(null);
    for (var i = 0; i < array.length; ++i) {
        var value = array[i];
        if (value in valuesSoFar) {
            return true;
        }
        valuesSoFar[value] = true;
    }
    return false;
}
```

**Time and space complexities**

>  EDIT ME

**Extra**: What if you have memory/space limitations and you need to minimize the use of memory/data structures.

**Solution**

> EDIT ME

**Time and space complexities**

>  EDIT ME

### Find key - extra

What if `A` is known to be sorted using unique values, can you improve the performance to find the key?

**Example of sorted and unique `A`**

```
function sortUniq(A) {
  if (A.length === 0) return A;
  A = A.sort();
  var ret = [A[0]];
  for (var i = 1; i < A.length; i++) {
    if (A[i-1] !== A[i]) {
      ret.push(A[i]);
    }
  }
  return ret;
}
```

**Solution**

```
function getFirstIndex(element){
  return A.indexOf(element);
}
```

**Time and space complexities**

> EDIT ME
