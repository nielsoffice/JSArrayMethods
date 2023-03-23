# JavaScript Working with Array Methods
JavaScript working with array method.

```JS
 // Array Slice 
 let arr = ['a','b','c','d','e'];
 
 // Slice the array BEGIN from key 2 
 console.log(arr.slice(2));   // Result: ['c','d','e']

 // Slice the array END from key 4  
 console.log(arr.slice(2, 4)); // Result: ['c','d']

 // Slice the array (minus) 2 means from key 2 removed! 
 console.log(arr.slice(-2)); // Result: ['d','e']
 console.log(arr.slice(-1)); // Result: ['e']
 
 // Slice the first array as "1" so removed a
 // Result: ['b','c','d','e']
 // removed last 2 as -2 which is "d" and "e" 
 // Result: ['b','c']
 console.log(arr.slice(1, -2)); // Result: ['b','c']
 
 // Reference: 
 // https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice
```

```JS
 // Array Reverse 
 let arr = ['a','b','c','d','e'];
 
 console.log(arr.reverse()); // Result: (5) ['e', 'd', 'c', 'b', 'a'] 
 
 // Reference: 
 // https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse
```

```JS
 // Array Concat or (combine array)
 let arr2 = [ 1, 2, 3, 4, 5 ];
 const letters = arr.concat(arr2);
 console.log(letters); // (10) ['e', 'd', 'c', 'b', 'a', 1, 2, 3, 4, 5]
 console.log([...arr, ...arr2]); // (10) ['e', 'd', 'c', 'b', 'a', 1, 2, 3, 4, 5]

 // Reference: 
 // https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat
```

```JS
 // Array JOIN
 console.log(letters.join(' - ')); // e - d - c - b - a - 1 - 2 - 3 - 4 - 5

 // Reference: 
 // https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join
```
