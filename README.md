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

```JS
 // Array at() 
 let arr = ['a','b','c','d','e'];

 // Getting first array element
 console.log(arr.at(0)); // Result: (5) ['a']  
 // Getting last array element
 console.log(arr.at(-1)); // Result: (5) ['e'] 
 
 // Reference: 
 // https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/at 
```

```JS
 // Array MAP|FILTER|REUCE
 [1,2,3,4].map(function(v,i) {
    
   // This like a forEach however this was made to map the array and data 
   // that create a brand new array of data that you need to workout !
   // ex. remove the key 2 
   ( i === 1 ) ? console.log( 2 +' from i') : console.log(v); // Result: 1 2 from i 3 4

 });

 const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
 const result = words.filter(word => word.length > 6);
 console.log(result);
 // Expected output: Array ["exuberant", "destruction", "present"]

 console.log('-------------REDUCE-------------');
 
 const array1 = [1, 2, 3, 4];
 // 0 + 1 + 2 + 3 + 4
 const initialValue = 0;
 const sumWithInitial = array1.reduce( function(accumulator, currentValue, index, array) {
   
   console.log('acc:' +accumulator);
   console.log('cval:' +currentValue);
   console.log('Index:' + index);
   console.log('d_array:' + array);

   return  accumulator + currentValue;

   },
  initialValue
 );

 console.log(sumWithInitial);
 // Expected output: 10

 // Reference:
 // https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
 // https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
 // https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce
```

```JS
// Which ARRAY METHOD TO USE

// *TO MUTATE ORIGINAL ARRAY
// Array method => add to original 
push(); // end
// Reference: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push

unshift(); // start
// Reference: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift

// Array method => Remove from original
pop(); // end
// Reference: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop

shift(); // start
// Reference: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift

splice(); // any
// Reference: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice

// ------------------------------------------------

// *A NEW ARRAY
// Computed from original:
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
map();

// Filtered using condition
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
filter();

// Portion of original
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice
slice();

// Combine array
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat
concat();

// Flattening the original
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/flat
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/flatMap
flat();
flatMap();

// ------------------------------------------------

// *A ARRAY INDEX
// Base on value
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf
indexOf 
// Base on test condition
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex
findIndex

// ------------------------------------------------

// *A ARRAY ELEMENT
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find
find();

// ------------------------------------------------

// *A ARRAY KNOW IF ARRAY INCLUDES certain element or not!
// Base on value
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes
includes();

// Base on a test condition
//https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some
some();
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every 
every();

// ------------------------------------------------

// *A ARRAY NEW STRING!
// Based on separator string
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join
join();
```
