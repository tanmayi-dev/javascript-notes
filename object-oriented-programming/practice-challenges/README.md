# Practice Challenges

### 1. Create a course roster using functions

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
