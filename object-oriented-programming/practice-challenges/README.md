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

#### Parameters for the Book object

- `title`: String
- `author`: String
- `quantity`: Number
- `edition`: String

#### Parameters for the ComicBook object

- `title`: String
- `author`: String
- `quantity`: Number
- `graphicArtist`: String

#### Book object functions

- `setEdition(newEdition)`: Sets the edition of the book
- `sell()`: Sells one copy of the book if there are available copies

#### Result

`[TestBook, TestComicBook]`: An array containing an instance of the `Book` object and an instance of the `ComicBook` object

#### Constraints

- You must use `defineProperty` to declare the `setEdition` function
- You must use `Object.create` to create a relationship between `Book` and `ComicBook`

#### Example 1 : 

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
