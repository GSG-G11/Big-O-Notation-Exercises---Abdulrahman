# Big O Notation Exercises-Abdulrahman

# Big O Notation Exercises

### Part 1

Simplify the following big O expressions as much as possible:

1. `O(n + 10)` => `O(n)`
2. `O(100 * n)` => `O(n)`
3. `O(25)`=> `O(1)`
4. `O(n^2 + n^3)` => `O(n^3)`
5. `O(n + n + n + n)` => `O(n)`
6. `O(1000 * log(n) + n)` => `O(n)`
7. `O(1000 * n * log(n) + n)` => `O(n * log(n))`
8. `O(2^n + n^2)` => `O(n^2)`
9. `O(5 + 3 + 1)` => `O(1)`
10. `O(n + n^(1/2) + n^2 + n * log(n)^10)` => `O(n^2)`

### Part 2

Determine the time and space complexities for each of the following functions. If you're not sure what these functions do, copy and paste them into the console and experiment with different inputs!

```js
// 1.
//Time efficiency => O(n)
//Space efficiency =>O(1)
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}

// 2.
//Time efficiency => O(1)
//Space efficiency =>O(1)
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}

// 3.
//Time efficiency => O(n)
//Space efficiency =>O(1)
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}

// 4.
//Time efficiency => O(n)
//Space efficiency =>O(n)
function onlyElementsAtEvenIndex(array) {
  let newArray = Array(Math.ceil(array.length / 2));
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray[i / 2] = array[i];
    }
  }
  return newArray;
}

// 5.
//Time efficiency => O(n^2)
//Space efficiency =>O(n)
function subtotals(array) {
  let subtotalArray = Array(array.length);
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray[i] = subtotal;
  }
  return subtotalArray;
}
```
