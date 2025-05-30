# Basic Javascript Problem Set 4 and Answer

> Click ⭐ if you like the Repository. You can Follow me [@SumonBarai](https://www.linkedin.com/in/sumonbarai/ "Sumon Barai") for technical updates.

## Table of Contents

## Javascript Problem

### Problem 1 :

Write a function `calculateStrikeRate` that takes in two parameters - the runs scored by a batsman and the total number of balls they faced. The function should return the batsman's strike rate, which is calculated as the number of runs scored per 100 balls faced.
For example, if the batsman scored 45 runs off 30 balls, their strike rate would be calculated as follows:
`(45 / 30) * 100 = 150`

The function should round the strike rate to two decimal places.  
Example Input/Output:

- calculateStrikeRate(45, 30) should return 150.00
- calculateStrikeRate(100, 60) should return 166.67
- calculateStrikeRate(25, 40) should return 62.50

<details>
<summary>Answer</summary>

```javaScript
function calculateStrikeRate(runs, balls) {
  const strikeRate = (runs / balls) * 100;
  return strikeRate.toFixed(2);
}

const result = calculateStrikeRate(100, 60);
console.log(result);
```

</details>

### Problem 2 :

Have the function `CountPairs` take in a string of lowercase letters and digits. The function should return the count of all pairs of characters in the string that add up to an even number.
For example, if the input string is "a1b2c3d4e5f6", there are 3 pairs that add up to an even number: "b2", "d4", and "f6". So the function should return 3.
If there are no such pairs, the function should return 0.
Examples:

- `CountPairs("a1b2c3d4e5f6")` should return 3
- `CountPairs("x1y2z3")` should return 1
- `CountPairs("a2b2c2d2")` should return 4

<details>
<summary>Answer</summary>

```javaScript
function CountPairs(color) {
  let count = 0;
  for (let i = 0; i < color.length; i += 2) {
    const digit = color[i + 1];
    if (parseInt(digit) % 2 === 0) {
      count++;
    }
  }

  return count;
}

const result = CountPairs("x1y7z8");
console.log(result);

```

</details>

### Problem 3 :

Write a function called `reverseString` that takes a string as input and returns the reverse of that string. Your function should not use the built-in `reverse()` method.
Example Input/Output:

- reverseString('hello') should return 'olleh'
- reverseString('racecar') should return 'racecar'
- reverseString('12345') should return '54321'

<details>
<summary>Answer</summary>

```javaScript
function reverseString(str) {
  let output = "";
  for (let i = str.length - 1; i >= 0; i--) {
    output += str[i];
  }

return output;
}

const result = reverseString("123456");
console.log(result);

or

function reverseString(str) {
let store = [];
let strArr = str.split("");
strArr.forEach((ele) => {
store.unshift(ele);
});

return store.join("");
}

```

</details>

### Problem 4 :

Write a function isPalindrome that takes in a string and returns true if the string is a palindrome (reads the same forwards and backwards) and false otherwise.
Example Input/Output:

- isPalindrome("racecar") should return true
- isPalindrome("hello") should return false
- isPalindrome("rotator") should return true
- isPalindrome("peep") should return true

<details>
<summary>Answer</summary>

```javaScript
function isPalindrome(str) {
  const reversed = str.split("").reverse().join("");
  return reversed === str ? true : false;
}

const result = isPalindrome("hello");
console.log(result);

or

function reverseString(str) {
let store = [];
let strArr = str.split("");
strArr.forEach((ele) => {
store.unshift(ele);
});

return store.join("");
}

```

</details>

### Problem 5 :

Write a function `mergeArrays` that takes in two arrays of integers and returns a new array that contains all the elements from both arrays, sorted in ascending order.
For example, if the two input arrays are:
[1, 3, 5, 7, 9]
[2, 4, 6, 8, 10]
The function should return the following array:
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Example Input/Output:

- mergeArrays([1, 3, 5, 7, 9], [2, 4, 6, 8, 10]) should return [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
- mergeArrays([2, 4, 6, 8, 10], [1, 3, 5, 7, 9]) should return [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
- mergeArrays([1, 2, 3], [4, 5, 6]) should return [1, 2, 3, 4, 5, 6]

<details>
<summary>Answer</summary>

```javaScript
function mergeArrays(arr1, arr2) {
  const mergeArr = arr1.concat(arr2);
  mergeArr.sort((a, b) => a - b);
  return mergeArr;
}

const result = mergeArrays([2, 4, 6, 8, 10], [1, 3, 5, 7, 9]);
console.log(result);

```

</details>

### Problem 6 :

Write a function called `findShortestWord` that takes in a string as a parameter and returns the shortest word in the string. If there are two or more words that are the same length and shortest, return the first word from the string with that length.

For example, if the input string is "The quick brown fox jumps over the lazy dog", the function should return "The".
Example Input/Output:

- findShortestWord("The quick brown fox jumps over the lazy dog") should return "The"
- findShortestWord("Hello world") should return "world"
- findShortestWord("Today is Monday") should return "is"

<details>
<summary>Answer</summary>

```javaScript
function findShortestWord(str) {
  const strArr = str.split(" ");
  let shortest = strArr[0];
  for (let i = 1; i < strArr.length; i++) {
    if (strArr[i].length < shortest.length) {
      shortest = strArr[i];
    }
  }

return shortest;
}

const result = findShortestWord(
"The quick brown fox jumps over the lazy dog"
);
console.log(result);

```

</details>

### Problem 7 :

Suppose you are building a student database for your class that will track student’s names and their marks. Your class has 40 students but now you are seeing that there are 41 entries in your database so you decide to check the database. And you find out that you have mistakenly uploaded a student’s name twice.
Task
Write a `removeDuplicates` function that takes in an array of names and returns a new array with any duplicates removed.
Sample Input:
Student_names =[
"Zara",
"Sadia",
"Mahin",
"Adnan",
"Maisha",
"Adnan",
"Faiyaz",
]
Sample Output :
Student_names = [‘Zara’, ‘Sadia’ , ‘Mahin’ , ‘Adnan’ , ‘Maisha’, ‘Faiyaz’]

<details>
<summary>Answer</summary>

```javaScript
function removeDuplicates(arr) {
  return new Set(arr);
}

const result = removeDuplicates([
  "Zara",
  "Sadia",
  "Mahin",
  "Adnan",
  "Maisha",
  "Adnan",
  "Faiyaz",
]);
console.log(result);


```

</details>

### Problem 8 :

Write a Javascript Program that takes String as a parameter and checks if the parameters are number or text. If the parameters are numbers then it will return a summation of the numbers. If the parameters are not numbers then it will generate a text by concatenating the strings.
Sample Input:
parseString(“21” , “24’ , “40”)
parseString(“Hello” , “Alpha”)
parseString(“Summer” , “2022”)
Sample Output:
85
Hello Alpha
Summer 2022

<details>
<summary>Answer</summary>

```javaScript
function parseString(...arr) {
  const isStrArr = arr.some((ele) => isNaN(ele));

  let result;
  if (isStrArr) {
    result = "";
    arr.forEach((item) => {
      result = result + " " + item;
    });
    return result;
  }

  if (!isStrArr) {
    result = 0;
    arr.forEach((item) => {
      result += parseInt(item);
    });
    return result;
  }
}

const result = parseString("10", "10", "10");
console.log(result);


```

</details>

### Problem 9 :

Given an array exists that has integers, write a function called "getPositiveNumbers" that takes the entire array as input and returns a new array containing only the positive numbers from the original array.
Sample Input : [2, -5, 10, -3, 8, -1, 0, 7]
Sample Output: [2, 10, 8, 7]

<details>
<summary>Answer</summary>

```javaScript
function getPositiveNumbers(numberArr) {
  let newNumberArr = [];
  for (let i = 0; i < numberArr.length; i++) {
    if (numberArr[i] > 0) {
      newNumberArr.push(numberArr[i]);
    }
  }

  return newNumberArr;
}

const result = getPositiveNumbers([2, -5, 10, -3, 8, -1, 0, 7]);
console.log(result);

```

</details>
