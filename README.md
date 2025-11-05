# Simple 52 javascript problem

> Click ⭐ if you like the Repository. You can Follow me [@SumonBarai](https://www.linkedin.com/in/sumonbarai/ "Sumon Barai") for technical updates.

### Problem 1 :

Print numbers from 1 to 10

<details>
<summary>Answer</summary>

```javaScript

for (let i = 1; i <= 10; i++) {
  console.log(i);
}

```

</details>

### Problem 2 :

Print the odd numbers less than 100

<details>
<summary>Answer</summary>

```javaScript

for (let i = 1; i <= 100; i++) {
  if (!(i % 2 === 0)) {
    console.log(i);
  }
}
```

</details>

### Problem 3 :

Print the multiplication table with 7

<details>
<summary>Answer</summary>

```javaScript

const multiplicationTable = (number) => {
  for (let i = 1; i <= 10; i++) {
    let row = `${number} * ${i} = ${number * i}`;
    console.log(row);
  }
};

multiplicationTable(7);

```

</details>

### Problem 4 :

Print all the multiplication tables with numbers from 1 to 10

<details>
<summary>Answer</summary>

```javaScript

const multiplicationFn = (number) => {
  for (let i = 1; i <= 10; i++) {
    let row = `${number} * ${i} = ${number * i}`;
    console.log(row);
  }
};
// run this multiplicationFn in 10 times
for (let i = 1; i <= 10; i++) {
  multiplicationFn(i);
  console.log("=========================");
}

```

</details>

### Problem 5 :

Calculate the sum of numbers from 1 to 10

<details>
<summary>Answer</summary>

```javaScript

const sumFn = (num) => {
  let sum = 0;
  for (let i = 1; i <= num; i++) {
    sum += i;
  }
  console.log(`Total Sum of ${num} is = ${sum}`);
};

sumFn(10);

```

</details>

### Problem 6 :

Calculate Factorial of 10 (10!)

<details>
<summary>Answer</summary>

```javaScript

function factorialFn(number) {
  let result = 1;
  for (let i = 1; i <= number; i++) {
    result *= i;
  }
  console.log(result);
}

factorialFn(10);

```

</details>

### Problem 7 :

Calculate the sum of odd numbers greater than 10 and less than 30

<details>
<summary>Answer</summary>

```javaScript

const sumOfOddNumber = (startNum, endNum) => {
  let result = 0;
  for (let i = startNum + 1; i < endNum; i++) {
    if (i % 2 === 1) {
      result += i;
    }
  }

  return result;
};

console.log(sumOfOddNumber(10, 30));

```

</details>

### Problem 8 :

Create a function that will convert from Celsius to Fahrenheit

<details>
<summary>Answer</summary>

```javaScript

const CelsiusToFahrenheit = (input) => {
  return input * (9 / 5) + 32;
};

const result = CelsiusToFahrenheit(20);

console.log(result);


```

</details>

### Problem 9 :

Create a function that will convert from Fahrenheit to Celsius

<details>
<summary>Answer</summary>

```javaScript

const fahrenheitToCelsius = (input) => {
  return ((input - 32) * 5) / 9;
};
const result = fahrenheitToCelsius(68);

console.log(result);


```

</details>

### Problem 10 :

Calculate the sum of numbers in an array of numbers

<details>
<summary>Answer</summary>

```javaScript

const sumOfArray = (input) => {
  let sum = 0;
  input.forEach((value) => {
    sum += value;
  });
  return sum;
};
const result = sumOfArray([1, 2, -3, 10]);
console.log(result);

```

</details>

### Problem 10 :

Calculate the sum of numbers in an array of numbers

<details>
<summary>Answer</summary>

```javaScript

const sumOfArray = (input) => {
  let sum = 0;
  input.forEach((value) => {
    sum += value;
  });
  return sum;
};
const result = sumOfArray([1, 2, -3, 10]);
console.log(result);

```

</details>

### Problem 11 :

Calculate the average of the numbers in an array of numbers

<details>
<summary>Answer</summary>

```javascript
const AverageOfArray = (input) => {
  if (!(input instanceof Array)) return "please submit valid input array";
  if (input.length === 0) return "please submit valid input array";
  let sum = 0;
  input.forEach((value) => {
    sum += value;
  });
  return sum / input.length;
};
const result = AverageOfArray([12, 20]);
console.log(result);
```

</details>

### Problem 12 :

Create a function that receives an array of numbers and returns an array containing only the positive numbers

<details>
<summary>Answer</summary>

```javascript
const filterPositiveNumber = (arr) => {
  const positiveArray = arr.filter((val) => val >= 0);
  return positiveArray;
};
const result = filterPositiveNumber([50, -30, 80]);
console.log(result);
```

</details>

### Problem 13 :

Find the maximum number in an array of numbers

<details>
<summary>Answer</summary>

```javascript
const maxNumber = (arr) => {
  return Math.max(...arr);
};
const result = maxNumber([50, -30, 100, 80]);
console.log(result);
```

</details>

### Problem 14 :

Print the first 10 Fibonacci numbers without recursion

<details>
<summary>Answer</summary>

```javascript
const fibonacciSeries = (limit) => {
  const series = [0, 1];
  for (let i = 0; i < limit - 2; i++) {
    series.push(series.at(-1) + series.at(-2));
  }
  return series;
};
const result = fibonacciSeries(10);

for (let i = 0; i < result.length; i++) {
  console.log(result[i]);
}
```

</details>

<details>
<summary>Answer</summary>

```javascript
let first = 0;
let second = 1;
let fib = [];
for (let i = 0; i < 6; i++) {
  fib.push(first);

  let next = first + second;
  first = second;
  second = next;
}
console.log(fib);
```

</details>

### Problem 15 :

Create a function that will find the nth Fibonacci number using recursion

<details>
<summary>Answer</summary>

```javascript
function findFibonacci(n) {
  if (n == 0) return 0;
  if (n == 1) return 1;
  return findFibonacci(n - 1) + findFibonacci(n - 2);
}
var n = findFibonacci(10);
console.log(n);
```

</details>

### Problem 16 :

Create a function that will return a Boolean specifying if a number is prime

<details>
<summary>Answer</summary>

```javascript
function isPrime(n) {
  if (n < 2) return false;
  if (n == 2) return true;

  var maxDiv = Math.sqrt(n);
  for (var i = 2; i <= maxDiv; i++) {
    if (n % i == 0) {
      return false;
    }
  }
  return true;
}

console.log(2, " is prime? ", isPrime(2));
console.log(3, " is prime? ", isPrime(3));
```

</details>

### Problem 17 :

Calculate the sum of digits of a positive integer number

<details>
<summary>Answer</summary>

```javascript
const sumOfDigits = (digits) => {
  if (typeof digits !== "number") {
    return "it is not possible to sum";
  }
  const convertToArray = digits.toString();
  let sum = 0;
  for (const iterator of convertToArray) {
    const convertToNumber = parseInt(iterator);
    sum += convertToNumber;
  }
  return sum;
};

const result = sumOfDigits(125);
console.log(`Sum of digit is = ${result}`);
```

</details>

### Problem 18 :

Print the first 100 prime numbers

<details>
<summary>Answer</summary>

```javascript
const isPrime = (num) => {
  if (num < 2) return false;
  if (num === 2) return true;

  const maxDiv = Math.sqrt(num);
  for (let i = 2; i <= maxDiv; i++) {
    if (num % i === 0) {
      return false;
    }
  }

  return true;
};

const printPrime = (num) => {
  let prime = [];
  for (let i = 0; i < num; i++) {
    if (isPrime(i)) {
      prime.push(i);
    }
  }
  return prime;
};

console.log(printPrime(100));
```

</details>

### Problem 19:

Create a function that will return in an array the first "nPrimes" prime numbers greater than a particular number "startAt"

<details>
<summary>Answer</summary>

```javascript
console.log(getPrime(10, 100));
function getPrime(nPrimes, startAt) {
  let arr = [];

  for (let i = startAt; arr.length < nPrimes; i++) {
    if (isPrime(i)) {
      arr.push(i);
    }
  }

  return arr;
}

function isPrime(num) {
  if (num < 2) return false;
  if (num === 2) return true;
  const maxDiv = Math.sqrt(num);
  for (let i = 2; i <= maxDiv; i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
}
```

</details>

### Problem 20:

Rotate an array to the left 1 position

<details>
<summary>Answer</summary>

```javascript
const arr = [2, 3, 5, 6, 7, 8];
const rotatedOnePositionLeft = (arr) => {
  const first = arr.shift();
  arr.push(first);
};
rotatedOnePositionLeft(arr);
console.log(arr);
```

</details>

### Problem 21:

Rotate an array to the right 1 position

<details>
<summary>Answer</summary>

```javascript
const arr = [2, 3, 5, 6, 7, 8];
const rotatedOnePositionRight = (arr) => {
  const last = arr.pop();
  arr.unshift(last);
};
rotatedOnePositionRight(arr);
console.log(arr);
```

</details>

### Problem 22:

Reverse an array

<details>
<summary>Answer</summary>

```javascript
const arr = [2, 3, 98, 986, 5, 6, 7, 8, 100, 85];
console.log(arr.reverse());
```

</details>

### Problem 23:

Reverse a string

<details>
<summary>Answer</summary>

```javascript
const demo = "Javascript";
const reverseArray = (str) => {
  const convertToArray = Array.from(str);
  const convertToNewArray = convertToArray.reverse();
  const result = convertToNewArray.join("");
  return result;
};

console.log(reverseArray(demo));
```

</details>

### Problem 24:

Create a function that will merge two arrays and return the result as a new array

<details>
<summary>Answer</summary>

```javascript
const arr1 = ["h", "k"];
const arr2 = ["ha", "ka"];

const mergeArr = (a, b) => {
  return a.concat(b);
};
console.log(mergeArr(arr1, arr2));
```

</details>

### Problem 25:

Create a function that will receive two arrays of numbers as arguments and return an array composed of all the numbers that are either in the first array or second array but not in both

<details>
<summary>Answer</summary>

```javascript
var ar1 = [1, 2, 3, 10, 5, 3, 14];
var ar2 = [1, 4, 5, 6, 14];

var ar = mergeExclusive(ar1, ar2);
console.log(ar);

function mergeExclusive(ar1, ar2) {
  var ar = [];

  for (let el of ar1) {
    if (!ar2.includes(el)) {
      ar.push(el);
    }
  }

  for (let el of ar2) {
    if (!ar1.includes(el)) {
      ar.push(el);
    }
  }

  return ar;
}
```

</details>

### Problem 26:

Create a function that will receive two arrays and will return an array with elements that are in the first array but not in the second

<details>
<summary>Answer</summary>

```javascript
const ar1 = [1, 2, 3, 10, 5, 3, 14];
const ar2 = [-1, 4, 5, 6, 14];

const searchAarry = (item1, item2) => {
  let newArray = [];
  for (let x of item1) {
    if (!item2.includes(x)) {
      newArray.push(x);
    }
  }
  return newArray;
};
console.log(searchAarry(ar1, ar2));
```

</details>

### Problem 27:

Create a function that will receive an array of numbers as argument and will return a new array with distinct elements

<details>
<summary>Answer</summary>

```javascript
// solution -1
const distinctArray = (array) => {
  let arr = [];
  array.forEach((item) => {
    if (!arr.includes(item)) {
      arr.push(item);
    }
  });
  return arr;
};
const a = [1, 1, 2, 3, 6, 8, 9, 8, 7, 2];
console.log(distinctArray(a));

// solution -2
const a = [1, 1, 2, 3, 6, 8, 9, 8, 7, 2];
const distinctArray2 = (arr) => {
  return [...new Set(arr)];
};
console.log(distinctArray2(a));
```

</details>

### Problem 28:

Calculate the sum of first 100 prime numbers

<details>
<summary>Answer</summary>

```javascript
// create is prime checker function
function isPrime(num) {
  if (num < 2) return false;
  if (num === 2) return true;
  const maxDiv = Math.sqrt(num);
  for (let i = 2; i <= maxDiv; i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
}

const sumOfPrimeNumber = (numberOfPrime) => {
  let prime = [];
  for (let i = 0; prime.length < numberOfPrime; i++) {
    if (isPrime(i)) {
      prime.push(i);
    }
  }
  return prime.reduce((total, curr) => total + curr, 0);
};
console.log(sumOfPrimeNumber(100));
```

</details>

### Problem 29:

Print the distance between the first 100 prime numbers

<details>
<summary>Answer</summary>

```javascript
const primeDistance = (numberOfPrime) => {
  const arr = [];
  for (let i = 0; arr.length < numberOfPrime; i++) {
    if (isPrime(i)) {
      arr.push(i);
    }
  }
  return arr;
};

// check prime number
const isPrime = (num) => {
  const SquareRoot = Math.sqrt(num);
  if (num < 2) return false;
  if (num === 2) return true;
  for (let i = 2; i <= SquareRoot; i++) {
    if (num % i === 0) return false;
  }
  return true;
};

const distance = (arr) => {
  for (let i = 0; i < arr.length; i++) {
    console.log(`${arr[i + 1]} - ${arr[i]} = ${arr[i + 1] - arr[i]}`);
  }
};
distance([1, 2, 3, 4]);
```

</details>

### Problem 30:

Create a function that will add two positive numbers of indefinite size. The numbers are received as strings and the result should be also provided as string.

<details>
<summary>Answer</summary>

```javascript
var n1 = "2909034221912398942349";
var n2 = "1290923909029309499";
var sum = add(n1, n2);

console.log(n1, "\n", n2, "\n", sum);

function add(sNumber1, sNumber2) {
  var s = "";
  var carry = 0;

  var maxSize = Math.max(sNumber1.length, sNumber2.length);

  for (var i = 0; i < maxSize; i++) {
    var digit1 = digitFromRight(sNumber1, i);
    var digit2 = digitFromRight(sNumber2, i);

    var sum = digit1 + digit2 + carry;
    var digitSum = sum % 10;
    carry = sum >= 10 ? 1 : 0;

    s = digitSum.toString() + s;
  }

  if (carry > 0) s = carry + s;

  return s;
}

function digitFromRight(s, digitNo) {
  if (digitNo >= s.length) return 0;

  var char = s[s.length - 1 - digitNo];
  return parseInt(char);
}
```

</details>

### Problem 31:

Create a function that will return the number of words in a text.

<details>
<summary>Answer</summary>

```javaScript
const numberOfWord = (sentence) => {
  return sentence.trim().split(" ").length;
};

const text =
  "Create a function that will capitalize the first letter of each word in a text";

console.log(numberOfWord(text));
```

</details>

### Problem 32:

Create a function that will capitalize the first letter of each word in a text.

<details>
<summary>Answer</summary>

```javaScript
const capitalizeFn = (sentence) => {
  const newArr = sentence.trim().split(" ");
  let capitalizeArr = [];
  newArr.forEach((word) => {
    const capitalized = word.charAt(0).toUpperCase() + word.slice(1);
    capitalizeArr.push(capitalized);
  });
  return capitalizeArr.join(" ");
};

const text =
  "   Create a function that will capitalize the first letter of each word in a text";

console.log(capitalizeFn(text));
```

</details>

### Problem 33:

Calculate the sum of numbers received in a comma delimited string.

<details>
<summary>Answer</summary>

```javaScript
const sumOfNumber = (str) => {
  const arr = str.split(",");
  let sum = 0;
  arr.forEach((element) => {
    const trim = element.trim();
    sum = sum + Number(trim);
  });
  return sum;
};

console.log(sumOfNumber("1,2, 3, 4"));
```

</details>

### Problem 34:

Create a function that will return an array with words inside a text.

<details>
<summary>Answer</summary>

```javaScript
const wordFn = (text) => {
  return text.split(" ");
};

var text =
  "Create a function, that will return an array (of string), with the words inside the text";

console.log(wordFn(text));
```

</details>

### Problem 35:

Create a function to convert a CSV text to a “bi-dimensional” array.

<details>
<summary>Answer</summary>

```javaScript
function csvToArray(data) {
  var arLines = data.split("\n");

  for (var i = 0; i < arLines.length; i++) {
    var arLine = arLines[i].split(";");
    arLines[i] = arLine;
  }

  return arLines;
}

var data =
  "John;Smith;954-000-0000\nMich;Tiger;305-000-0000\nMonique;Vasquez;103-000-0000";

var ar = csvToArray(data);
console.log(JSON.stringify(ar));
```

</details>

### Problem 36:

Create a function that converts a string to an array of characters.

<details>
<summary>Answer</summary>

```javaScript
const convertToArr = (str) => {
  return Array.from(str);
};

console.log(convertToArr("i love bangladesh"));
```

</details>

### Problem 37:

Create a function that will convert a string into an array containing the ASCII codes of each character.

<details>
<summary>Answer</summary>

```javaScript
function getCharCodes(str) {
  let ascii = [];
  for (let i = 0; i < str.length; i++) {
    const code = str.charCodeAt(i);
    ascii.push(code);
  }
  return ascii;
}

console.log(getCharCodes("I like JavaScript"));
```

</details>

### Problem 38:

Create a function that will convert an array containing ASCII codes into a string.

<details>
<summary>Answer</summary>

```javaScript
const ASCIICodeToString = (arr) => {
  return String.fromCharCode(...arr);
};

console.log(
  ASCIICodeToString([
    73, 32, 108, 105, 107, 101, 32, 74, 97, 118, 97, 83, 99, 114, 105, 112, 116,
  ])
);
```

</details>

### Problem 39:

Implement the Caesar cipher (encryption and decryption).

<details>
<summary>Answer</summary>

```javaScript
var text = "I LOVE JAVASCRIPT";
var textEnc = encrypt(text, 13);
var textDec = decrypt(textEnc, 13);

console.log(text);
console.log(textEnc);
console.log(textDec);

function decrypt(msg, key) {
  return encrypt(msg, key * -1);
}

function encrypt(msg, key) {
  var encMsg = "";

  for (var i = 0; i < msg.length; i++) {
    var code = msg.charCodeAt(i);

    if (code >= 65 && code <= 90) { // 'A' to 'Z'
      code -= 65;
      code = mod(code + key, 26);
      code += 65;
    }

    encMsg += String.fromCharCode(code);
  }

  return encMsg;
}

function mod(n, p) {
  if (n < 0) n = p - (Math.abs(n) % p);
  return n % p;
}
```

</details>

### Problem 40:

Implement the bubble sort algorithm for an array of numbers.

<details>
<summary>Answer</summary>

```javaScript
var ar = [23, 1000, 1, -1, 8, 3];
console.log(ar);
bubbleSort(ar);
console.log(ar);

function bubbleSort(ar) {
  var shouldSort = true;
  var length = ar.length;

  while (shouldSort) {
    shouldSort = false;
    length--;

    for (var i = 0; i < length; i++) {
      var a = ar[i];
      if (a > ar[i + 1]) {
        ar[i] = ar[i + 1];
        ar[i + 1] = a;
        shouldSort = true;
      }
    }
  }
}
```

</details>

### Problem 41:

Create a function to calculate the distance between two points defined by their x, y coordinates.

<details>
<summary>Answer</summary>

```javaScript
const distance = (x1, y1, x2, y2) => {
  return Math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2);
};

console.log(distance(1, 2, 4, 6));
```

</details>

### Problem 42:

Create a function that will return a Boolean indicating if two circles defined by center coordinates and radius are intersecting.

<details>
<summary>Answer</summary>

```javaScript
function collisionCircleCircle(circle1X, circle1Y, circle1R, circle2X, circle2Y, circle2R) {
  return (
    getDistance(circle1X, circle1Y, circle2X, circle2Y) <= circle1R + circle2R
  );
}

function getDistance(x1, y1, x2, y2) {
  var l1 = x2 - x1;
  var l2 = y2 - y1;
  return Math.sqrt(l1 * l1 + l2 * l2);
}

console.log(collisionCircleCircle(200, 200, 100, 300, 300, 50));
```

</details>

### Problem 43:

Create a function that will receive a bi-dimensional array and a number and will extract the specified column as a unidimensional array.

<details>
<summary>Answer</summary>

```javaScript
var ar = [
  ["John", 120],
  ["Jane", 115],
  ["Thomas", 123],
  ["Mel", 112],
  ["Charley", 122],
];

const extract = (arr, column) => {
  let newArray = [];
  for (let test of arr) {
    newArray.push(test[column]);
  }
  return newArray;
};

console.log(extract(ar, 1));
```

</details>

### Problem 44:

Create a function that will convert a string containing a binary number into a number.

<details>
<summary>Answer</summary>

```javaScript
function binaryToNumber(sBinary) {
  return parseInt(sBinary, 2);
}

console.log(binaryToNumber("111110101111"));
```

</details>

### Problem 45:

Create a function to calculate the sum of all the numbers in a jagged array (numbers or arrays of numbers on unlimited levels).

<details>
<summary>Answer</summary>

```javaScript
var ar = [1, 2, [15, [23], [5, 12]], [100]];

const sum = (arr) => {
  const newArray = arr.flat(Infinity);
  return newArray.reduce((total, current) => total + current, 0);
};

console.log(sum(ar));
```

</details>

### Problem 46:

Find the maximum number in a jagged array of numbers or arrays.

<details>
<summary>Answer</summary>

```javaScript
const ar1 = [2, 4, 10, [12, 4, [100, 99], 4], [3, 2, 99], 0];

const maximumNumber = (arr) => {
  const newArray = arr.flat(Infinity);
  return `maximum = ${Math.max(...newArray)}`;
};

console.log(maximumNumber(ar1));
```

</details>

### Problem 47:

Deep copy a jagged array with numbers or other arrays into a new array.

<details>
<summary>Answer</summary>

```javaScript
const ar1 = [2, 4, 10, [12, 4, [100, 99], 4], [3, 2, 99], 0];
const ar2 = JSON.parse(JSON.stringify(ar1));
ar2[0] = 100;

console.log(ar1);
console.log(ar2);
```

</details>

### Problem 48:

Create a function to return the longest word(s) in a string.

<details>
<summary>Answer</summary>

```javaScript
const String =
  "Create a function to return the longest word(s) in a sentance sg";

const longestWord = (text) => {
  const longestArray = [];
  let longest = "";

  const convertedToArray = text.split(" ");

  for (let word of convertedToArray) {
    if (word.length > longest.length) {
      longest = word;
      longestArray[0] = word;
    } else if (word.length === longest.length) {
      longestArray.push(word);
    }
  }

  if (longestArray.length > 1) {
    return longestArray;
  } else {
    return longest;
  }
};

console.log(longestWord(String));
```

</details>

### Problem 49:

Shuffle an array of strings.

<details>
<summary>Answer</summary>

```javaScript
const arr = ["Shuffle", "an", "array", "of", "strings"];

function randomNumberGenerator(min, max) {
  return Math.floor(Math.random() * (max - min)) + min;
}

const ShuffleArray = (arr) => {
  const container = new Set();
  const targetedLoop = arr.length;
  for (let i = 0; container.size < targetedLoop; i++) {
    const number = randomNumberGenerator(0, targetedLoop);
    container.add(arr[number]);
  }
  return [...container];
};

console.log(ShuffleArray(arr));
```

</details>

### Problem 50:

Create a function that will receive `n` as argument and return an array of `n` unique random numbers from 1 to `n`.

<details>
<summary>Answer</summary>

```javaScript
const getRandomNumber = (n) => {
  const uniqueSet = new Set();
  for (let i = 0; uniqueSet.size < n; i++) {
    const randomNumber = randomNumberGenerator(1, n);
    uniqueSet.add(randomNumber);
  }
  return [...uniqueSet];
};

const randomNumberGenerator = (min, max) => {
  return Math.floor(Math.random() * (max - min + 1)) + min;
};

console.log(getRandomNumber(10));
```

</details>

### Problem 51:

Find the frequency of characters inside a string. Return the result as an array of objects. Each object has 2 fields: character and number of occurrences.

<details>
<summary>Answer</summary>

```javaScript
function getCharFrequency(text) {
  var ar = [];

  for (var chr of text) {
    updateFrequency(ar, chr);
  }

  return ar;
}

function updateFrequency(ar, chr) {
  for (var el of ar) {
    if (el.chr === chr) {
      el.count++;
      return;
    }
  }

  ar.push({ chr: chr, count: 1 });
}

var ar = getCharFrequency("Find the frequency of characters inside a string");
console.log(JSON.stringify(ar));
```

</details>

### Problem 52:

Calculate Fibonacci(500) with high precision (all decimals).

<details>
<summary>Answer</summary>

```javaScript
function fibonacci(n) {
  if (n === 0) return "0";
  if (n === 1) return "1";

  var n1 = "0";
  var n2 = "1";

  for (var i = 2; i <= n; i++) {
    var sum = add(n1, n2);
    n1 = n2;
    n2 = sum;
  }

  return n2;
}

function add(sNumber1, sNumber2) {
  var maxSize = Math.max(sNumber1.length, sNumber2.length);

  var s1 = sNumber1.padStart(maxSize, "0");
  var s2 = sNumber2.padStart(maxSize, "0");

  var s = "";
  var carry = 0;

  for (var i = maxSize - 1; i >= 0; i--) {
    var digit1 = parseInt(s1[i]);
    var digit2 = parseInt(s2[i]);

    var sum = digit1 + digit2 + carry;
    var digitSum = sum % 10;
    carry = sum >= 10 ? 1 : 0;

    s = digitSum.toString() + s;
  }

  if (carry > 0) s = carry + s;

  return s;
}

console.log(fibonacci(500));
```
