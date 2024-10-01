# Practice Challenges

#### Index

1. [Create a course roster using functions](#p1)
2. [Create a Book object with functions](#p2)

   
### 1. Create a course roster using functions <a id="p1"></a>

[solution](./01-create-a-roster-with-functions.js)

Create a `Student` object and a `CourseRoster` object, and use their prototype settings to create `getRoster()` and `returnGraduatingStudents()` object functions. The output of these object functions is described below/

**Parameters for the Student Object**
- `name`: String
- `grades`: An array of integers that rangee from 0-100

**Student Object Functions**
- `getGrades`: Returns the grades for the student
- `checkIsPassing`: Returns true if the student is passing (use the provided `calculateGPA` function)

**Parameters for the CourseRoster object**
- `roster`: An array of `Student` objects
- `teacher`: String

**CourseRoster object functions**
- `getRoster`: Returns a string of student names separated by a comma
- `returnGraduatingStudents`: Returns an array of Student objects who will graduate

**Result**
- `testCourseRoster`: An instance of the CourseRoster object

**Example 1**

Input:
```js
const roster = [
    {
        name: 'Anwar',
        grades: [97, 87, 99]
    },
    {
        name: 'Sophie',
        grades: [75, 22, 85]
    },
    {
        name: 'Ron',
        grades: [64, 77, 90]
    }
];
const teacher = 'Harriet'
```

Result:
```js
CourseRoster {
    roster: [
        Student { name: 'Anwar', grades: [Array] },
        Student { name: 'Sophie', grades: [Array] },
        Student { name: 'Ron', grades: [Array] }
    ],
    teacher: 'Harriet'
}
```

--- 

### 2. Create a Book object with functions <a id="p2"></a>

[solution](./02-create-a-book-object-with-functions.js)

We can use the `Object.defineProperty()` method to define a new property directly on an object. This method takes the object where the property is defined, the property name we want to define, and a descriptor of the property we're defining.

For example, if we have a `wrangler` object, we can define a new property called `maker` which sets its maker to "Jeep":

```js
const wrangler = {};

Object.defineProperty(wrangler, 'maker', {
    value : 'Jeep'
});

wrangler.maker; // Jeep
```

Similarly, `Object.create()` allows us to create a new object using an already-existing object as the prototype.

**Your task**: Create a `Book` object and a `ComicBook` object. For the `Book` object, define a `setEdition` property and a `sell()` function. For the `ComicBook` object, use `Object.create()` to create a relationship between `Book` and `ComicBook`.

**Parameters for the Book object**

- `title`: String
- `author`: String
- `quantity`: Number
- `edition`: String

**Parameters for the ComicBook object**

- `title`: String
- `author`: String
- `quantity`: Number
- `graphicArtist`: String

**Book object functions**

- `setEdition(newEdition)`: Sets the edition of the book
- `sell()`: Sells one copy of the book if there are available copies

**Result**

`[TestBook, TestComicBook]`: An array containing an instance of the `Book` object and an instance of the `ComicBook` object

**Constraints**

- You must use `defineProperty` to declare the `setEdition` function
- You must use `Object.create` to create a relationship between `Book` and `ComicBook`

**Example 1 :** 

Input : 
```js
const bookData = {
    title: 'Pride and Prejudice',
    author: 'Emily Bronte',
    quantity: 3,
    edition: 4
}

const comicBookData = {
    title: 'Spiderman',
    author: 'Stan Lee',
    quantity: 3.
    graphicArtist: 'Todd McFarlane'
}
```

Result :
```js
[
    Book {
        title: 'Pride and Prejudice',
        author: 'Emily Bronte',
        quantity: 2,
        edition: 5
    },
    ComicBook {
        title: 'Spiderman',
        author: 'Stan Lee',
        quantity: 3,
        edition: undefined,
        graphicArtist: 'Todd McFarlane'
    }
]
```

---

### 3. Create a Country with Classes

[solution](./03-create-a-country-with-classes.js)

JavaScript class syntax is a method of creating objects, built on prototypes. Classes use a constructor function which is a special way to initialize objects. Classes can also contain functions that both modify and return data as in this example:

```js
class Person {
   constructor(name, age) {
      this.name = name;
      this.age = age;
   }

   sayHello() {
      return 'Hello!';
   }

   haveBirthday() {
      this.age = this.age + 1;
   }
}
```

**Your task**: Create a `Country` class with two internal methods : `getOverview()` and `setPopulation()`.

**Parameters for the Country class**

- `name`: String
- `continent`: String
- `currency`: String
- `population`: String

**Country class functions**

- `getOverview()`: Returns an overview of the country's data (for example, _"France is a country in Europe. Its currency is the Euro and it has a current population of 67.75 million people."_)
- `setPopulation(newPopulation)`: Sets the population for a country

**Result**

`testCountry`: An instance of the `Country` class

**Constraints**

- You must use JavaScript class syntax
- `getOverview` must return a string with the following syntax:
  ```
  [country] is a country in [continent]. Its currency is the [currency] and it has a current population of [population] people.
  ```

**Example 1 :**

Input:
```js
const countryData = {
   name: 'France',
   continent: 'Europe',
   currency: 'Euro',
   population: '67.75 million'
}
```

Result:
```js
Country {
   name: 'France',
   continent: 'Europe',
   currency: 'Euro',
   population: '70.12 million'
}
```
