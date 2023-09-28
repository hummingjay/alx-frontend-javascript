
# 0x02. ES6 classes

## Tasks

### 0. You used to attend a place like this at some point

Implement a class named `ClassRoom`:

  - Prototype: `export default class ClassRoom`
  - It should accept one attribute named `maxStudentsSize` (Number) and assigned to `_maxStudentsSize`

File: [0-classroom.js](0-classroom.js)

### 1. Let's make some classrooms

Import the `ClassRoom` class from `0-classroom.js`.

Implement a function named `initializeRooms`. It should return an array of 3 `ClassRoom` objects with the sizes 19, 20, and 34 (in this order).

File: [1-make\_classrooms.js](1-make_classrooms.js)

### 3. Methods, static methods, computed methods names..... MONEY

Implement a class named Currency:

  - Constructor attributes:
    - `code` (String)
    - `name` (String)
  - Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
  - Implement a getter and setter for each attribute.
  - Implement a method named displayFullCurrency that will return the attributes in the following format name (code).

