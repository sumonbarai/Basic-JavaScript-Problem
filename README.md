# Simple 20 javascript problem

> Click ⭐ if you like the Repository. You can Follow me [@SumonBarai](https://www.linkedin.com/in/sumonbarai/ "Sumon Barai") for technical updates.

### Problem 1 :

Given an array of numbers , find the smallest number
`const arr = [20, 60, 80, -60, -90, 40, 12, 600, 81, 1]`

<details>
<summary>Solution 1</summary>

```javaScript
const smallNumber = Math.min(...arr);
console.log(smallNumber);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
const ascendingOrder = arr.sort((a, b) => {
  return a - b;
});

const smallestNumber = ascendingOrder.at(0);
console.log(smallestNumber);
```

</details>

<details>
<summary>Solution 3</summary>

```JavaScript
function findSmallest(arr) {
    return arr.reduce((smallest, current) => {
        return current < smallest ? current : smallest;
    });
}
console.log(findSmallest([20, 60, 80, -60, -90, 40, 12, 600, 81, 1]));

```

</details>

<details>
<summary>Solution 4</summary>

```JavaScript
function findMin(arr) {
    let min = arr[0];
    arr.forEach(num => {
        if(num < min) min = num;
    });
    return min;
}
console.log(findMin([20, 60, 80, -60, -90, 40, 12, 600, 81, 1]));
```

</details>

<details>
<summary>Solution 5</summary>

```JavaScript
function getSmallestNumber(arr) {
    let smallest = arr[0];
    for(let i = 1; i < arr.length; i++) {
        if(arr[i] < smallest) {
            smallest = arr[i];
        }
    }
    return smallest;
}
console.log(getSmallestNumber([20, 60, 80, -60, -90, 40, 12, 600, 81, 1]));
```

</details>

### Problem 2 :

Given an array of numbers , find the largest number  
const arr = [20, 60, 80, -60, -90, 40, 12, 600, 81, 1];

<details>
<summary>Solution 1</summary>

```JavaScript
const largestNumber = Math.max(...arr);
console.log(largestNumber);

const ascendingOrder = arr.sort((a, b) => {
  return a - b;
});
const largestNumber = ascendingOrder.at(-1);
console.log(largestNumber);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
function findLargest(arr) {
    return arr.reduce((max, current) => {
        return current > max ? current : max;
    });
}
console.log(findLargest([20, 60, 80, -60, -90, 40, 12, 600, 81, 1]));
```

</details>

<details>
<summary>Solution 3</summary>

```JavaScript
function getLargestNumber(arr) {
    let largest = arr[0];
    for(let i = 1; i < arr.length; i++) {
        if(arr[i] > largest) {
            largest = arr[i];
        }
    }
    return largest;
}
console.log(getLargestNumber([20, 60, 80, -60, -90, 40, 12, 600, 81, 1]));
```

</details>

<details>
<summary>Solution 4</summary>

```JavaScript
function findMax(arr) {
    let max = arr[0];
    arr.forEach(num => {
        max = num > max ? num : max;
    });
    return max;
}
console.log(findMax([20, 60, 80, -60, -90, 40, 12, 600, 81, 1]));
```

</details>

## Problem 3 :

Given an array of numbers , find the sum of all number  
`const arr = [1, 2, 3, 4, 5, 10];`

<details>
<summary>Solution 1</summary>

```JavaScript
const sumOfNumber = arr.reduce((total, current) => {
  return total + current;
}, 0);
console.log(sumOfNumber);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
function getSum(arr) {
    return eval(arr.join('+'));
}
console.log(getSum([1, 2, 3, 4, 5, 10]));
```

</details>

<details>
<summary>Solution 3</summary>

```JavaScript
function sumArray(arr) {
    let sum = 0;
    arr.forEach(num => sum += num);
    return sum;
}
console.log(sumArray([1, 2, 3, 4, 5, 10]));
```

</details>

<details>
<summary>Solution 4</summary>

```JavaScript
function sumNumbers(arr) {
    let sum = 0;
    for (const num of arr) {
        sum += num;
    }
    return sum;
}
console.log(sumNumbers([1, 2, 3, 4, 5, 10]));
```

</details>

## Problem 4 :

Given an array of Strings , create a new array with the first letter of each string  
`const arr = ["hello", "word", "foo", "bar"];`

<details>
<summary>Solution 1</summary>

```JavaScript
let newArr = [];
arr.forEach((val) => {
  newArr.push(val.slice(0, 1));
});
console.log(newArr);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
let newArr = [];
for (let i = 0; i < arr.length; i++) {
  newArr.push(arr[i][0]);
}
console.log(newArr);
```

</details>

<details>
<summary>Solution 3</summary>

```JavaScript
const average = arr => arr.reduce((a, b) => a + b) / arr.length;
console.log(average([1, 2, 3, 4, 5]));
```

</details>

## Problem 5 :

Given an array of numbers, create a new array with only even numbers  
`const arr = [1, 2, 3, 4, 5, 6];`

<details>
<summary>Solution 1</summary>

```JavaScript
const newArr = arr.filter((num) => {
  if (num % 2 === 0) {
    return num;
  }
  return false;
});

console.log(newArr);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
function getEvenNumbers(arr) {
    let result = [];
    arr.forEach(num => {
        if (num % 2 === 0) result.push(num);
    });
    return result;
}
console.log(getEvenNumbers([1, 2, 3, 4, 5, 6]));
```

</details>

<details>
<summary>Solution 1</summary>

```JavaScript
function findEvenNumbers(arr) {
    let result = [];
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] % 2 === 0) {
            result.push(arr[i]);
        }
    }
    return result;
}
console.log(findEvenNumbers([1, 2, 3, 4, 5, 6]));
```

</details>

<details>
<summary>Solution 1</summary>

```JavaScript
const evenNumbers2 = [1, 2, 3, 4, 5, 6].reduce((acc, curr) => {
    if (curr % 2 === 0) acc.push(curr);
    return acc;
}, []);
console.log(evenNumbers2);
```

</details>

## Problem 6 :

Given an array of Strings , find the longest string  
`const arr = ["hw", "hello", "wordss", "foo", "bar"];`

<details>
<summary>Solution 1</summary>

```JavaScript
const arr = ["hw", "hello", "wordss", "foo", "bar"]
let longest = arr[0];
arr.forEach((val) => {
  if (val.length > longest.length) {
    longest = val;
  }
});
console.log(longest);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
const findLongest = (arr) => {
    return arr.reduce((longest, current) => {
        return current.length > longest.length ? current : longest;
    });
};
console.log(findLongest(arr));
```

</details>

<details>
<summary>Solution 3</summary>

```JavaScript
function getLongestString(arr) {
    return arr.sort((a, b) => b.length - a.length)[0];
}
console.log(getLongestString(arr));
```

</details>

## Problem 7 :

Given an array of Numbers , find the average  
`const arr = [1, 2, 3, 4, 5];`

<details>
<summary>Solution 1</summary>

```JavaScript
const arr = [1, 2, 3, 4, 5];
const average = (num) => {
  const total = num.reduce((total, current) => {
    return total + current;
  }, 0);
  return total / num.length;
};

console.log(average(arr));
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
function avarage(arr) {
  let sum = 0;
  arr.forEach((num) => {
    sum += num;
  });
  const avg = sum / arr.length; // avg is short form of avarage
  return avg;
}

console.log(avarage([1, 2, 3, 4, 5]));
```

</details>

<details>
<summary>Solution 3</summary>

```JavaScript
function avarage(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  const avg = sum / arr.length;
  return avg;
}

console.log(avarage([1, 2, 3, 4, 5]));

Solution 3
function avarage(arr) {
  return eval(arr.join("+")) / arr.length;
}

console.log(avarage([1, 2, 3, 4, 5]));
```

</details>

## Problem 8 :

Given an array of strings , sort them in alphabetical order  
`const arr = ["man", "can", "Do", "apple", "everything"];`

<details>
<summary>Solution 1</summary>

```JavaScript
const arr = ["man", "can", "Do", "apple", "everything"];
const result = arr.sort();
console.log(result);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
const sortedArr = arr.sort((a, b) => {
  if (a.toUpperCase() < b.toUpperCase()) return -1;
  if (a.toUpperCase() > b.toUpperCase()) return 1;
});
console.log(sortedArr);
```

</details>

<details>
<summary>Solution 1</summary>

```JavaScript
const arr = ["man", "can", "Do", "apple", "everything"];
const result = arr.sort((a, b) => a.localeCompare(b));
console.log(result);
```

</details>

## Problem 9 :

Given an array of numbers , remove the all duplicates  
`const arr = [1, 2, 3, 4, 5, 5, 2, 8]`

<details>
<summary>Solution 1</summary>

```JavaScript
const arr = [1, 2, 3, 4, 5, 5, 2, 8];

const uniqueArray = [...new Set(arr)];
console.log(uniqueArray);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
const arr = [1, 2, 3, 4, 5, 5, 2, 8];

const uniqueArray = [];
arr.forEach((num) => {
  if (!uniqueArray.includes(num)) {
    uniqueArray.push(num);
  }
});

console.log(uniqueArray);
```

</details>

<details>
<summary>Solution 3</summary>

```JavaScript
const uniqueArray = arr.filter((num, index) => arr.indexOf(num) == index);
console.log(uniqueArray);

Solution 04 reduce()
const uniqueArray = arr.reduce((unique, num) => {
  if (!unique.includes(num)) {
    unique.push(num);
  }
  return unique;
}, []);

console.log(uniqueArray);
```

</details>

## Problem 10

Given an array of integers , find two numbers the add up to a target value  
`const numbers = [2, 7, 11, 15]`
`const target = 9;`

<details>
<summary>Solution 1</summary>

```JavaScript
const numbers = [2, 7, 11, 15];
const target = 9;
for (let i = 0; i < numbers.length; i++) {
  for (let j = i + 1; j < numbers.length; j++) {
    if (numbers[i] + numbers[j] === target) {
      console.log(numbers[i], numbers[j]);
    }
  }
}
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
const numbers = [2, 7, 11, 15];
const target = 9;

function twoSum(numbers, target) {
  let left = 0;
  let right = numbers.length - 1;

  while (left < right) {
    let currentSum = numbers[left] + numbers[right];

    if (currentSum === target) {
      return [numbers[left], numbers[right]];
    } else if (currentSum < target) {
      left++;
    } else {
      right--;
    }
  }
  return [];
}

console.log(twoSum(numbers, target));

```

</details>

## Problem 11 :

a food ordering app needs to sort the menu items by price

```javascript
const menuItem = [
  { name: "burger", price: 5.99 },
  { name: "fries", price: 2.99 },
  { name: "soda", price: 1.99 },
  { name: "pizza", price: 10.99 },
];
```

<details>
<summary>Solution 1</summary>

```JavaScript
menuItem.sort((a, b) => {
  return a.price - b.price;
});
console.log(menuItem);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
for (let i = 0; i < menuItem.length; i++) {
  for (let j = i + 1; j < menuItem.length; j++) {
    if (menuItem[i].price > menuItem[j].price) {
      [menuItem[i], menuItem[j]] = [menuItem[j], menuItem[i]];
    }
  }
}
console.log(menuItem);
```

</details>

## Problem 12 :

A social media app needs to find all unique hashtags used in a users posts

```javascript
const userPost = [
  "just we want for a #run #fitness",
  "enjoying the #weekend #friends",
  "can't wait #run for the #vacation #beach",
];
```

<details>
<summary>Solution 1</summary>

```JavaScript
const uniqueHashTag = new Set();

for (let post of userPost) {
  const words = post.split(" ");
  words.forEach((word) => {
    if (word.startsWith("#")) {
      const actualWord = word.slice(1);
      uniqueHashTag.add(actualWord);
    }
  });
}

console.log(uniqueHashTag);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
function getUniqueHashtags(arr) {
  const regExHashtag = /#\w+/g;
  const hashtags = arr.flatMap((post) => post.match(regExHashtag) || []);
  return [...new Set(hashtags)];
}

console.log(getUniqueHashtags(userPost));
```

</details>

## Problem 13 :

A weather app needs to formate a list of temperatures in celsius and fahrenheit for display

`const temperatures = [12, 25, 8, 19, 3]`

<details>
<summary>Solution 1</summary>

```JavaScript
const temperatures = [12, 25, 8, 19, 3]; // is celsius temperature

const formatedTemparature = temperatures.map((celsius) => {
  const fahrenheit = celsius * 1.8 + 32;
  return `${celsius} °C (${fahrenheit.toFixed(1)})°F`;
});
console.log(formatedTemparature);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
function celsiusToFahrenheit(tempArray) {
  const convertedTemp = [];
  tempArray.forEach((value) => {
    const fahrenheit = value * 1.8 + 32;
    convertedTemp.push(`${value} °C (${fahrenheit.toFixed(1)})°F`);
  });
  return convertedTemp;
}
console.log(celsiusToFahrenheit(temperatures));
```

</details>

<details>
<summary>Solution 3</summary>

```JavaScript
function celsiusToFahrenheit(tempArray) {
  const convertedTemp = [];

  for (let i = 0; i < tempArray.length; i++) {
    const fahrenheit = tempArray[i] * 1.8 + 32;
    convertedTemp.push(`${tempArray[i]} °C (${fahrenheit.toFixed(1)})°F`);
  }

  return convertedTemp;
}

console.log(celsiusToFahrenheit(temperatures));

```

</details>

## Problem 14 :

A video sharing site need to keep track of the number o f views, like and comments on each video

```JavaScript
const videos = [
  {
    id: 1,
    title: "how code is run",
    views: 1000,
    comments: [{ id: 1, text: "very usefully" }],
  },
  {
    id: 2,
    title: "how code is run",
    views: 2000,
    comments: [{ id: 1, text: "very thanks" }],
  },
];
```

<details>
<summary>Solution 1</summary>

```JavaScript
function incrementView(id) {
  const video = videos.find((v) => {
    return v.id === id;
  });

  if (video) {
    video.views += 1;
  }
  console.log(video);
}
function addComment(id, comment) {
  const video = videos.find((v) => {
    return v.id === id;
  });

  if (video) {
    video.comments.push({ id: video.comments.length + 1, text: comment });
  }
  console.log(video);
}

incrementView(1);
addComment(1, "i am very happy");
addComment(1, "i am very happy");

```

</details>

## Problem 15 :

Facebook needs to keep track of the number of reactions (like, love haha wow sad,angry) on each post

```JavaScript
const videos = [
  {
    id: 1,
    title: "how code is run",
    comments: [{ id: 1, text: "very usefully" }],
    reactions: {
      like: 50,
      love: 100,
      haha: 20,
      wow: 15,
      sad: 1,
      angry: 0,
    },
  },
  {
    id: 2,
    title: "how code is run",
    comments: [{ id: 1, text: "very thanks" }],
    reactions: {
      like: 150,
      love: 1100,
      haha: 120,
      wow: 115,
      sad: 11,
      angry: 10,
    },
  },
];
```

<details>
<summary>Solution 1</summary>

```JavaScript
const incrementReaction = function (id, type) {
  const post = videos.find((v) => {
    return v.id === id;
  });
  if (post) {
    post.reactions[type] = post.reactions[type] + 1;
  }
};
incrementReaction(1, "haha");
incrementReaction(2, "love");
console.log(videos);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
const addReaction = (postId, reactionType) => {
    return videos.map(video => {
        if (video.id === postId) {
            return {
                ...video,
                reactions: {
                    ...video.reactions,
                    [reactionType]: video.reactions[reactionType] + 1
                }
            };
        }
        return video;
    });
};

// Test the function
const updatedVideos = addReaction(1, "haha");
console.log(updatedVideos);
```

</details>

## Problem 16 :

Based on finding the two numbers that add up to a target value  
`const purchases = [1, 2, 3, 4, 5, 1, 3, 5, 6, 7, 2, 4, 8, 9, 9]`  
`let target = 10;`

<details>
<summary>Solution 1</summary>

```JavaScript
for (let i = 0; i < purchases.length; i++) {
  for (let j = i + 1; j < purchases.length; j++) {
    if (purchases[i] + purchases[j] === target) {
      pairs.push([purchases[i], purchases[j]]);
    }
  }
}
console.log(pairs);
```

</details>

<details>
<summary>Solution 1</summary>

```JavaScript
function twoSum(arr, target) {
  const sortedArr = [...arr].sort((a, b) => a - b);
  let left = 0;
  let right = sortedArr.length - 1;
  let pairs = [];

  while (left < right) {
	let currentSum = sortedArr[left] + sortedArr[right];

	if (currentSum === target) {
	  pairs.push([sortedArr[left], sortedArr[right]]);
	  left++;
	  right--;
	} else if (currentSum < target) {
	  left++;
	} else {
	  right--;
	}
  }
  return pairs;
}

console.log(twoSum(purchases, target));
```

</details>

## Problem 17 :

A restaurant wants to keep track of its inventory of ingredients for various dishes . the restaurants chefs need to be able to easily update the inventory levels for each ingredient as then use them in dishes

```JavaScript
const ingredients = [
  { name: "dough", inventory: 10 },
  { name: "tomato sauce", inventory: 8 },
  { name: "mozzarella cheese", inventory: 6 },
  { name: "mushrooms", inventory: 3 },
];
```

<details>
<summary>Solution 1</summary>

```JavaScript
const updateInventory = (name, quantity) => {
  const ingredient = ingredients.find((item) => {
    return item.name === name;
  });
  if (ingredient) {
    if (ingredient.inventory > 0) {
      ingredient.inventory -= quantity;
    }
  } else {
    console.log(`${name} is not found`);
  }
};
updateInventory("dough", 2);
console.log(ingredients);
```

</details>

## Problem 18 :

Given an array of object representing products sort the products by price from lowest to height

```JavaScript
const products = [
  { name: "iphone 1", price: 1000 },
  { name: "iphone 2", price: 8000 },
  { name: "iphone 3", price: 60000 },
  { name: "iphone 4", price: 3000 },
]
```

<details>
<summary>Solution 1</summary>

```JavaScript
products.sort((a, b) => a.price - b.price);
console.log(products);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
function sortByPrice(arr) {
  for (let i = 0; i < arr.length; i++) {
    for (let j = i + 1; j < arr.length; j++) {
      if (arr[i].price > arr[j].price) {
        [arr[i], arr[j]] = [arr[j], arr[i]];
      }
    }
  }
  return arr;
}

console.log(sortByPrice(products));
```

</details>

## Problem 19 :

Suppose you have an array of objects representing people and you wants to filter the array to only include people ,who are over 18 years old

```JavaScript
const peoples = [
  { name: "ali", age: 75 },
  { name: "ali khan", age: 55 },
  { name: "ali suni", age: 15 },
  { name: "ali bali", age: 10 },
  { name: "ali sho", age: 20 },
]
```

<details>
<summary>Solution 1</summary>

```JavaScript
const adult = peoples.filter((people) => people.age >= 18);
console.log(adult);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
function adultsOnly(arr) {
  return arr.reduce((adults, person) => {
    if (person.age >= 18) {
      adults.push(person);
    }
    return adults;
  }, []);
}

console.log(adultsOnly(peoples));
```

</details>

<details>
<summary>Solution 3</summary>

```JavaScript
function adultsOnly(arr) {
  for (let i = arr.length - 1; i >= 0; i--) {
    if (arr[i].age < 18) {
      arr.splice(i, 1);
    }
  }
}

adultsOnly(peoples);
console.log(peoples);
```

</details>

## Problem 20 :

In a web application that displays a list of product with their prices in different currencies . lets say that we have an array of products ,where each product has a name and a price property USD. we want to display a list of these products with prices converted to a different currency, based on the users preferences.

```JavaScript
const products = [
  { name: "iphone 1", price: 1000 },
  { name: "iphone 2", price: 8000 },
  { name: "iphone 3", price: 60000 },
  { name: "iphone 4", price: 3000 },
];
```

</details>

<details>
<summary>Solution 1</summary>

```JavaScript
const exchangeRate = 0.009090909;

const ProductPriceByUSD = products.map((product) => {
  const price = (product.price * exchangeRate).toFixed(2);
  return { ...product, price: Number(price) };
});

console.log(ProductPriceByUSD);
```

</details>

<details>
<summary>Solution 2</summary>

```JavaScript
function priceConverter(array, exchangeRate = 122.9356) {
  let convertedArray = [];
  array.forEach((item) => {
    const convertedPrice = Number((item.price * exchangeRate).toFixed(2));
    console.log(typeof convertedPrice);
    convertedArray.push({ ...item, price: convertedPrice });
  });

  return convertedArray;
}

console.log(priceConverter(products));
```

</details>
