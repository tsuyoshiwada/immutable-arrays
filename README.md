# immutable-arrays

Immutable versions of normally mutable array methods

[![Build Status](https://travis-ci.org/georapbox/immutable-arrays.svg?branch=master)](https://travis-ci.org/georapbox/immutable-arrays)
[![npm version](https://badge.fury.io/js/immutable-arrays.svg)](http://badge.fury.io/js/immutable-arrays)
[![Dependencies](https://david-dm.org/georapbox/immutable-arrays.svg?theme=shields.io)](https://david-dm.org/georapbox/immutable-arrays)
[![devDependency Status](https://david-dm.org/georapbox/immutable-arrays/dev-status.svg)](https://david-dm.org/georapbox/immutable-arrays#info=devDependencies)

## Install

```sh
$ npm install immutable-arrays
```

## Test

```sh
$ npm test
```

## Functions

<dl>
<dt><a href="#immutablePush">immutablePush(array, ...elementN)</a> ⇒ <code>Array</code></dt>
<dd><p>Adds one or more elements to the end of an array by returning a new array instead of mutating the original one.</p></dd>
<dt><a href="#immutablePop">immutablePop(array)</a> ⇒ <code>Array</code></dt>
<dd><p>Removes the last element from an array by returning a new array instead of mutating the original one.</p></dd>
<dt><a href="#immutableDelete">immutableDelete(array, index)</a> ⇒ <code>Array</code></dt>
<dd><p>Deletes an element from an array by its index in the array.</p></dd>
<dt><a href="#immutableShift">immutableShift(array)</a> ⇒ <code>Array</code></dt>
<dd><p>Removes the first element from an array.</p></dd>
<dt><a href="#immutableUnshift">immutableUnshift(array, ...elementN)</a> ⇒ <code>Array</code></dt>
<dd><p>Adds one or more elements to the beginning of an array.</p></dd>
<dt><a href="#immutableReverse">immutableReverse(array)</a> ⇒ <code>Array</code></dt>
<dd><p>Reverses an array (not in place). The first array element becomes the last, and the last array element becomes the first.</p></dd>
<dt><a href="#immutableSort">immutableSort(array, [compareFunction])</a> ⇒ <code>Array</code></dt>
<dd><p>Sorts the elements of an array (not in place) and returns a sorted array.</p></dd>
<dt><a href="#immutableSplice">immutableSplice(array, [start], [deleteCount], [...elementN])</a> ⇒ <code>Array</code></dt>
<dd><p>Removes existing elements and/or adds new elements to an array.</p></dd>
</dl>

<a name="immutablePush"></a>

## immutablePush(array, ...elementN) ⇒ <code>Array</code>
Adds one or more elements to the end of an array by returning
a new array instead of mutating the original one.

**Returns**: <code>Array</code> - A new array with the new entries added to the end.  

| Param | Type | Description |
| --- | --- | --- |
| array | <code>Array</code> | The original array. |
| ...elementN | <code>\*</code> | The elements to add to the end of the array. |

**Example**  
```js
const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutablePush(originalArray, 'f', 'g');
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['a', 'b', 'c', 'd', 'e', 'f', 'g']
```

<a name="immutablePop"></a>

## immutablePop(array) ⇒ <code>Array</code>
Removes the last element from an array by returning
a new array instead of mutating the original one.

**Returns**: <code>Array</code> - A new array with the last element removed.  

| Param | Type | Description |
| --- | --- | --- |
| array | <code>Array</code> | The original array. |

**Example**  
```js
const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutablePop(originalArray);
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['a', 'b', 'c', 'd']
```

<a name="immutableDelete"></a>

## immutableDelete(array, index) ⇒ <code>Array</code>
Deletes an element from an array by its index in the array.

**Returns**: <code>Array</code> - A new array with the element removed.  

| Param | Type | Description |
| --- | --- | --- |
| array | <code>Array</code> | The original array. |
| index | <code>Number</code> | The index of the element to delete in the original array. |

**Example**  
```js
const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableDelete(originalArray, 2);
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['a', 'b', 'd', 'e']
```

<a name="immutableShift"></a>

## immutableShift(array) ⇒ <code>Array</code>
Removes the first element from an array.

**Returns**: <code>Array</code> - A new array with the first element removed.  

| Param | Type | Description |
| --- | --- | --- |
| array | <code>Array</code> | The original array. |

**Example**  
```js
const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableShift(originalArray);
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['b', 'c', 'd', 'e']
```

<a name="immutableUnshift"></a>

## immutableUnshift(array, ...elementN) ⇒ <code>Array</code>
Adds one or more elements to the beginning of an array.

**Returns**: <code>Array</code> - A new array with the new elements added to the front.  

| Param | Type | Description |
| --- | --- | --- |
| array | <code>Array</code> | The original array. |
| ...elementN | <code>\*</code> | [description] The elements to add to the front of the array. |

**Example**  
```js
const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableUnshift(originalArray, 'f', 'g');
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['f', 'g', 'a', 'b', 'c', 'd', 'e']
```

<a name="immutableReverse"></a>

## immutableReverse(array) ⇒ <code>Array</code>
Reverses an array (not in place).
The first array element becomes the last, and the last array element becomes the first.

**Returns**: <code>Array</code> - A new array reversed.  

| Param | Type | Description |
| --- | --- | --- |
| array | <code>Array</code> | The original array. |

**Example**  
```js
const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableReverse(originalArray);
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['e', 'd', 'c', 'b', 'a']
```

<a name="immutableSort"></a>

## immutableSort(array, [compareFunction]) ⇒ <code>Array</code>
Sorts the elements of an array (not in place) and returns a sorted array.

**Returns**: <code>Array</code> - A new sorted array.

| Param | Type | Description |
| --- | --- | --- |
| array | <code>Array</code> | The original array. |
| [compareFunction] | <code>Function</code> | Specifies a function that defines the sort order. If omitted, the array is sorted according to each character's Unicode code point value, according to the string conversion of each element. |

**Example**  
```js
const numberArray = [20, 3, 4, 10, -3, 1, 0, 5];
const stringArray = ['Blue', 'Humpback', 'Beluga'];

const resultArray = immutableSort(numberArray, (a, b) => a - b);
// -> numberArray [20, 3, 4, 10, -3, 1, 0, 5]
// -> resultArray [-3, 0, 1, 3, 4, 5, 10, 20]

const resultArray = immutableSort(numberArray, (a, b) => b - a);
// -> numberArray [20, 3, 4, 10, -3, 1, 0, 5]
// -> resultArray [20, 10, 5, 4, 3, 1, 0, -3]

const resultArray = immutableSort(stringArray);
// -> stringArray ['Blue', 'Humpback', 'Beluga']
// -> resultArray ['Beluga', 'Blue', 'Humpback']

const resultArray = immutableSort(stringArray, (a, b) => a.toLowerCase() < b.toLowerCase());
// -> stringArray ['Blue', 'Humpback', 'Beluga']
// -> resultArray ['Humpback', 'Blue', 'Beluga']
```

<a name="immutableSplice"></a>

## immutableSplice(array, [start], [deleteCount], [...elementN]) ⇒ <code>Array</code>
Removes existing elements and/or adds new elements to an array.

**Returns**: <code>Array</code> - The result array.  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| array | <code>Array</code> |  | The original array. |
| [start] | <code>Number</code> | <code>array.length</code> | Zero based index at which to start changing the array.        If greater than the length of the array, actual starting index will be set to the length of the array. |
| [deleteCount] | <code>Number</code> | <code>array.length - start</code> | An integer indicating the number of old array elements to remove.        If `deleteCount` is 0, no elements are removed.        If `deleteCount` is lower than 0, `deleteCount` will be equal to 0.        If `deleteCount` is greater than the number of elements left in the array starting at        `start`, then all of the elements through the end of the array will be deleted.        If `deleteCount` is omitted, `deleteCount` will be equal to (`array.length - start`),        i.e., all of the elements beginning with `start` index on through the end of the array will be deleted. |
| [...elementN] | <code>\*</code> |  | The elements to add to the array, beginning at the start index.        If you don't specify any elements, will only remove elements from the array. |

**Example**  
```js
const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableSplice(originalArray, 0);
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray []

const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableSplice(originalArray, 0, 1);
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['b', 'c', 'd', 'e']

const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableSplice(originalArray, 0, 3);
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['d', 'e']

const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableSplice(originalArray, 0, originalArray.length);
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray []

const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableSplice(originalArray, 0, -3);
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['a', 'b', 'c', 'd', 'e']

const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableSplice(originalArray, 0, 0, 'lorem', 'ipsum');
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['lorem', 'ipsum', 'a', 'b', 'c', 'd', 'e']

const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableSplice(originalArray, originalArray.length, 0, 'lorem', 'ipsum');
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['a', 'b', 'c', 'd', 'e', 'lorem', 'ipsum']

const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableSplice(originalArray, 0, 2, 'lorem', 'ipsum');
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['lorem', 'ipsum', 'c', 'd', 'e']

const originalArray = ['a', 'b', 'c', 'd', 'e'];
const resultArray = immutableSplice(originalArray, originalArray.length - 2, 2, 'lorem', 'ipsum');
// -> originalArray ['a', 'b', 'c', 'd', 'e']
// -> resultArray ['a', 'b', 'c', 'lorem', 'ipsum']
```

## License

[The MIT License (MIT)](https://georapbox.mit-license.org/@2017)
