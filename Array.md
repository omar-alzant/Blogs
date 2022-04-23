# Array Methods:

<h2> Code used: <a href="https://www.w3schools.com/js/"> javascript </a> </h2>

## Methods -1-  contain the basics:

<ol>
  <li>
    <h3>
    instanceof():
    </h3>
    <h5>
    The instanceof operator tests to see if the prototype property of a constructor appears anywhere in the prototype chain of an object. The return value is a boolean value.
    </h5>
  </li>
  

```javascript
  function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
const auto = new Car('Honda', 'Accord', 1998);

console.log(auto instanceof Car);
// expected output: true
```

  <li>
    <h3>
      toString( ):
    </h3>
    <h5>
      The JavaScript method toString() converts an array to a string of (comma separated) array values
    </h5>
  </li>

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
// Banana,Orange,Apple,Mango
```

  <li>
   <h3> 
    pop( ):
  </h3>
  <h5>
  The pop() method removes the last element from an array:
  </h5>
</li>

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo1").innerHTML = fruits;
fruits.pop();
// Banana,Orange,Apple,Mango

document.getElementById("demo2").innerHTML = fruits;
// Banana,Orange,Apple
```

  <li>
    <h3>
      push( ):
    </h3> 
    <h5>
      The push() method appends a new element to an array:
    </h5>
  </li>

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo1").innerHTML = fruits;
fruits.push("Kiwi");
// Banana,Orange,Apple,Mango

document.getElementById("demo2").innerHTML = fruits;
// Banana,Orange,Apple,Mango,Kiwi

```
  <li>
  <h3>
      shift( ):
  </h3>
  <h5>
    The shift() method removes the first element of an array (and "shifts" the other elements to the left):
  </h5>
  </li>

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo1").innerHTML = fruits;
fruits.shift();
//Banana,Orange,Apple,Mango

document.getElementById("demo2").innerHTML = fruits;
// Orange,Apple,Mango
```

<li>
  <h3>
    unshift( ):
  </h3>
  <h5>
    The unshift() method adds a new element to an array (at the beginning), and "unshifts" older elements.
    </h5>
    <h5>
The unshift() method returns the new array length.
  </h5>
</li>

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo1").innerHTML = fruits.unshift("Lemon");
// 5 

document.getElementById("demo2").innerHTML = fruits;
// Lemon,Banana,Orange,Apple,Mango
```

  <li>
    <h3>
    length( ):
  </h3>
  <h5>
The length property provides an easy way to append new elements to an array without using the push() method:
  </h5>
</li>

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo1").innerHTML = fruits;
fruits[fruits.length] = "Kiwi";
document.getElementById("demo2").innerHTML = fruits;
// Banana,Orange,Apple,Mango,Kiwi
```


<h4>
<h2>Warning !</h2>
Array elements can be deleted using the JavaScript operator `delete`.
Using delete leaves undefined holes in the array.
Use `pop()` or `shift()` instead.
</h4>

**********************************************

<li>
<h3>
  Concat():
</h3>  
  <h5> 
    The concat() method creates a new array by merging (concatenating) existing arrays:
  </h5>
  <em><strong>
  The concat() method does not change the existing arrays. It always returns a new array.

  </em></strong>
</li>

```javascript
const myGirls = ["Cecilie", "Lone"];
const myBoys = ["Emil", "Tobias", "Linus"];
const myChildren = myGirls.concat(myBoys);

document.getElementById("demo").innerHTML = myChildren;
// Cecilie,Lone,Emil,Tobias,Linus
```

<h5>
The concat() method merges (concatenates) arrays:

</h5>

```javascript
const array1 = ["Cecilie", "Lone"];
const array2 = ["Emil", "Tobias", "Linus"];
const array3 = ["Robin", "Morgan"];

const myChildren = array1.concat(array2, array3); 

document.getElementById("demo").innerHTML = myChildren;

//  Cecilie,Lone,Emil,Tobias,Linus,Robin,Morgan
```

<h5>
The concat() method can merge string values to arrays:

</h5>

```javascript
const myArray = ["Emil", "Tobias", "Linus"];
const myChildren = myArray.concat("Peter"); 
document.getElementById("demo").innerHTML = myChildren;

//  Emil,Tobias,Linus,Peter
``` 

<li>
  <h3>
  Splice():
  </h3>
  <h5>
  The splice() method can be used to add new items to an array:
  </h5>
 
</li>


```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo1").innerHTML = fruits;

fruits.splice(2, 0, "Lemon", "Kiwi");
document.getElementById("demo2").innerHTML = fruits;

//  Banana,Orange,Lemon,Kiwi,Apple,Mango
```
<ul>
<li>
The first parameter (2) defines the position where new elements should be added (spliced in).
</li>
<li>
The second parameter (0) defines how many elements should be removed.
</li>
<li>
The rest of the parameters ("Lemon" , "Kiwi") define the new elements to be added.
</li>
</ul>


<h5>
The splice() method returns an array with the deleted items:
</h5>


```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo1").innerHTML = "Original Array:<br> " + fruits;

// Original Array:
// Banana,Orange,Apple,Mango


let removed = fruits.splice(2, 2, "Lemon", "Kiwi"); 
document.getElementById("demo2").innerHTML = "New Array:<br>" + fruits;

// New Array:
// Banana,Orange,Lemon,Kiwi


document.getElementById("demo3").innerHTML = "Removed Items:<br> " + removed; 

// Removed Items:
// Apple,Mango
```


<h5>
With clever parameter setting, you can use splice() to remove elements without leaving "holes" in the array:

</h5>

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo1").innerHTML = fruits;
fruits.splice(0, 1);
document.getElementById("demo2").innerHTML = fruits;

//Orange,Apple,Mango
```
<ul>
<li>
The first parameter (0) defines the position where new elements should be added (spliced in).
</li>
<li>
The second parameter (1) defines how many elements should be removed.
</li>
<li>
The rest of the parameters are omitted. No new elements will be added.
</li>
</ul>

<li>
<h3>
Slice():  ~~different to Splice !!
</h3>
<h5>
This  example slices out a part of an array starting from array element 1 ("Orange"):
</h5>
</li>


```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1);
document.getElementById("demo").innerHTML = fruits + "<br><br>" + citrus;

//  Orange,Lemon,Apple,Mango

const citrus = fruits.slice(3);
document.getElementById("demo").innerHTML = fruits + "<br><br>" + citrus;

// Apple,Mango
```


<h2>Note</h2>
<h5>
The slice() method creates a new array.
</h5>
<h5>
The slice() method does not remove any elements from the source array.
</h5>

*********************************************

<ul>
<li>
The slice() method can take two arguments like slice(1, 3).
</li>
<li>
The method then selects elements from the start argument, and up to (but not including) the end argument.
</li>
</ul>

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1,3);

// Banana,Orange,Lemon,Apple,Mango

document.getElementById("demo").innerHTML = fruits + "<br><br>" + citrus;

// Orange,Lemon

```

*********************************
<h2>
Split():::   String to Array :::
</h2>
  
<strong>
split() splits a string into an array of substrings, and returns the array

</strong>


```javascript

let text = "How are you doing today?";
const myArray = text.split(" ");

document.getElementById("demo").innerHTML = myArray[1]; 

//  are

const elements = ['Fire', 'Air', 'Water'];

console.log(elements.join());
// expected output: "Fire,Air,Water"
```

****************************************



</ol>



## Methods -2- Advanced method for Array :

<ol>

  <li>
    <h3>
      Reverse():
    </h3>
    <h5>
      The reverse() method reverses an array in place. The first array element becomes the last, and the last array element becomes the first.
    </h5>
  </li>
  
  ```javascript
    const array1 = ['one', 'two', 'three'];
console.log('array1:', array1);

// expected output: "array1:" Array ["one", "two", "three"]
  ```

<li>
    <h3>
      Reduce():
  </h3>
  <h5>    
    array.reduce(function(total, currentValue, currentIndex, arr), initialValue)
  </h5>
  
  <table>
    <tr>
      <th> Parameter </th>
      <th>  Description </th> 
    </tr>
    <tr>
      <td> total </td>
      <td> 
        <ul>
          <li>Required.</li>
          <li> The initialValue, or the previously returned value of the function.  </li>
        </ul>
      </td>
    </tr>     
    <tr>      
       <td> currentValue </td>
      <td> 
        <ul>
          <li>Required.</li>
          <li> The value of the current element.
          </li>
        </ul>
      </td>
    </tr> 
    <tr>
        <td> currentIndex </td>       
      <td> 
        <ul>
          <li>Optional.</li>
          <li> The index of the current element.</li>
        </ul>
      </td>
    </tr>
    <tr>
        <td> arr </td>
      <td> 
        <ul>
          <li>Optional.</li>
          <li> The array the current element belongs to.</li>
        </ul>
      </td>
  </tr>
  <tr>
      <td> initialValue </td>
  <td> 
        <ul>
          <li>Optional.</li>
          <li>  A value to be passed to the function as the initial value.</li>
        </ul>
      </td>
  </tr>
  </table>
  
  </li>
  
  
  ```javascript
  const sum = function(sum) {
	let s = sum.reduce((t,num)=>{
    return (t+num);
  },0);
  return s;
};

  // another example ::
  
const multiply = function(mult) {
  let m = mult.reduce((total,m) =>{
    return (total*m);
  },1);
  return m 
  // console.log(m)
};
  ```
  
  
  <strong>
      An Advanced Example:
  </strong>
  
  ```javascript
	const data = ['car', 'car', 'truck', 'truck', 'bike', 'walk', 'car', 'van', 'bike', 'walk', 'car', 'van', 'car', 'truck', 'pogostick'];

    const transportation = data.reduce(function(obj, item) {
      if (!obj[item])  // const data.obj = {} ----- data.obj.item
      {
        obj[item] = 0;
      }
      obj[item]++;
      return obj;
    }, {});

/*	bike: 2
	car: 5
	pogostick: 1
	truck: 3
	van: 2
	walk: 2 
*/
```

	
***************************
	<p> Another example with object</p>
	
```javascript
const inventors = [
      { first: 'Albert', last: 'Einstein', year: 1879, passed: 1955 },
      { first: 'Isaac', last: 'Newton', year: 1643, passed: 1727 },
      { first: 'Galileo', last: 'Galilei', year: 1564, passed: 1642 },
      { first: 'Marie', last: 'Curie', year: 1867, passed: 1934 },
      { first: 'Johannes', last: 'Kepler', year: 1571, passed: 1630 },
      { first: 'Nicolaus', last: 'Copernicus', year: 1473, passed: 1543 },
      { first: 'Max', last: 'Planck', year: 1858, passed: 1947 },
      { first: 'Katherine', last: 'Blodgett', year: 1898, passed: 1979 },
      { first: 'Ada', last: 'Lovelace', year: 1815, passed: 1852 },
      { first: 'Sarah E.', last: 'Goode', year: 1855, passed: 1905 },
      { first: 'Lise', last: 'Meitner', year: 1878, passed: 1968 },
      { first: 'Hanna', last: 'Hammarström', year: 1829, passed: 1909 }
    ];

	const people = [
      'Bernhard, Sandra', 'Bethea, Erin', 'Becker, Carl', 'Bentsen, Lloyd', 'Beckett, Samuel', 'Blake, William', 'Berger, Ric', 'Beddoes, Mick', 'Beethoven, Ludwig',
      'Belloc, Hilaire', 'Begin, Menachem', 'Bellow, Saul', 'Benchley, Robert', 'Blair, Robert', 'Benenson, Peter', 'Benjamin, Walter', 'Berlin, Irving',
      'Benn, Tony', 'Benson, Leana', 'Bent, Silas', 'Berle, Milton', 'Berry, Halle', 'Biko, Steve', 'Beck, Glenn', 'Bergman, Ingmar', 'Black, Elk', 'Berio, Luciano',
      'Berne, Eric', 'Berra, Yogi', 'Berry, Wendell', 'Bevan, Aneurin', 'Ben-Gurion, David', 'Bevel, Ken', 'Biden, Joseph', 'Bennington, Chester', 'Bierce, Ambrose',
      'Billings, Josh', 'Birrell, Augustine', 'Blair, Tony', 'Beecher, Henry', 'Biondo, Frank'
    ];
	   
	
	//  How many years did all the inventors live?


    const totalYears = inventors.reduce((total, inventor) => {
      return total + (inventor.passed - inventor.year);
    }, 0);    

    // inventors.reduce((total, a) => { ... }, let total = 0  ) 
	
	// 861
	
```	
  
  
<li>
	<h3>
		Map():	
	</h3>
	<h5>
		The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.
	</h5>
</li>
	
  
```javascript
    const fullNames = inventors.map(inventor => `${inventor.first} ${inventor.last}`);
	/*
	0: "Albert Einstein"
1: "Isaac Newton"
2: "Galileo Galilei"
3: "Marie Curie"
4: "Johannes Kepler"
5: "Nicolaus Copernicus"
6: "Max Planck"
7: "Katherine Blodgett"
8: "Ada Lovelace"
9: "Sarah E. Goode"
10: "Lise Meitner"
11: "Hanna Hammarström"
length: 12
	*/
```
  
  ```javascript
	const numbers = [65, 44, 12, 4];
	const newArr = numbers.map(myFunction);

	document.getElementById("demo").innerHTML = newArr;

	function myFunction(num) {
  		return num * 10;
	}

//  Multiply every element in the array with 10:

//	650,440,120,40	
```
  
```javascript
	const books = [
      {
        title: 'Book',
        author: 'Name'
      },
      {
        title: 'Book2',
        author: 'Name2'
      }
    ]
	
const getTheTitles = function(books) {    
let l = b.map((tit) => `${tit.title}`)
return l;
};

// ['Book','Book2']
	
```


### Sort the inventors by birthdate, oldest to youngest : 
	
	```javascript
	    const ordered = inventors.sort((a, b) => a.year > b.year ? 1 : -1);
	```		
```	
//	first: "Lise"
//last: "Meitner"
//passed: 1968
//year: 1878

//	first: "Max"
//last: "Planck"
//passed: 1947
//year: 1858
	
	//first: "Isaac"
//last: "Newton"
//passed: 1727
//year: 1643

//...
```
	
### Sort the inventors by years lived : 	

	```javascript
	const oldest = inventors.sort(function(a, b) {
	const lastInventor = a.passed - a.year;
      	const nextInventor = b.passed - b.year;
      
      // if(lastInventor > nextInentor) return -1;
      //  else return 1;

      return lastInventor > nextInventor ? -1 : 1;
    });
	```
```
//	0: {first: 'Lise', last: 'Meitner', year: 1878, passed: 1968}
//	1: {first: 'Max', last: 'Planck', year: 1858, passed: 1947}
//	2: {first: 'Isaac', last: 'Newton', year: 1643, passed: 1727}
//	3: {first: 'Katherine', last: 'Blodgett', year: 1898, passed: 1979}
//...
```
	
### Sort the people alphabetically by last name : 
	
	
	```javascript
	const alpha = people.sort((lastOne, nextOne) => {
      	const [aLast, aFirst] = lastOne.split(', ');
      	const [bLast, bFirst] = nextOne.split(', ');
      return aLast > bLast ? 1 : -1;
    });
	```
	
```	
//0: "Beck, Glenn"
//1: "Becker, Carl"
//2: "Beckett, Samuel"
//3: "Beddoes, Mick"
//4: "Beecher, Henry"
//5: "Beethoven, Ludwig"
//6: "Begin, Menachem"
//7: "Belloc, Hilaire"
// ...
```

	
<li>
	<h3>	Filter():</h3>
	<h5>	The filter() method creates a new array with all elements that pass the test implemented by the provided function. </h5>
</li>
	
	```javascript
		    const fifteen = inventors.filter(inventor => (inventor.year >= 1500 && inventor.year < 1600));
	```
```
// 0: {first: 'Galileo', last: 'Galilei', year: 1564, passed: 1642}
//1: {first: 'Johannes', last: 'Kepler', year: 1571, passed: 1630}
```
													  
	```javascript
		const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
		const result = words.filter(word => word.length > 6);

		// expected output: Array ["exuberant", "destruction", "present"]
	```
	
	
	
	
```javascript
	const people = [
      { name: 'Wes', year: 1988 },
      { name: 'Kait', year: 1986 },
      { name: 'Irv', year: 1970 },
      { name: 'Lux', year: 2015 }
    ];

    const comments = [
      { text: 'Love this!', id: 523423 },
      { text: 'Super good', id: 823423 },
      { text: 'You are the best', id: 2039842 },
      { text: 'Ramen is my fav food ever', id: 123523 },
      { text: 'Nice Nice Nice!', id: 542328 }
    ];	
```
		
	```javascript
		    const isAdult = people.some(person => ((new Date()).getFullYear()) - person.year >= 19);
	// isAdult: true
	```
	
	```javascript
	    const allAdults = people.every(person => ((new Date()).getFullYear()) - person.year >= 19);
	// 	allAdults: false
	```
	
	```javascript
		    const comment = comments.find(comment => comment.id === 823423);
	// id: 823423
	// text: "Super good"
	```
	
</ol>
































