# Mutable vs Immutable

## 1. Javascript Datatypes

### Primitive type:

```js
1. String
2. Number
3. Boolean
4. Undefined
5. Null
6. BigInt
7. Symbols
```

### Reference type:

```js
1. Array
2. Object
3. Function / Class
4. Map
5. Set
```

## 2. Primitive type:

```js
const name1 = "mr nobody";
let name2 = name1;
console.log("name2: ", name2);
name2 = "jhon";
console.log("name2: ", name2);
console.log("name1: ", name1);
```

## 3. Reference type:

#### Array:

```js
const array1 = [1, 2, 3];
console.log("array1: ", array1);
let array2 = array1;
console.log("array2: ", array2);
array2[0] = 1000;
console.log("array2: ", array2);
console.log("array1: ", array1);
```

#### How to solve it?

```js
let array2 = [...array1];
```

### Objects:

```js
const user = {
  name: "mr nobody"
}
const newUser = user;
newUser.name = "john"
console.log("user: ", user);
console.log("newUser: ", newUser);
```

#### How to solve it?

```js
const newUser = { ...user };
```

## 4. Reference type using the map:

```js
const users = [
  {
    name: "mr nobody",
    age: 20
  },
  {
    name: "john",
    age: 30
  }
];
const newArray = users.map((user) => {
  const today = new Date();
  user.age = today.getFullYear() - user.age;
  return user;
});
console.table("newArray: ", newArray);
console.table("users: ", users);
```

#### How to solve it?

```js
return {
    ...user,
    year: today.getFullYear() - user.age
  };
```


## 5. Advantages of the immutability:

- No side effects
- Work with large data structure of inmutable data

## 6. Disadvantages / trade off of the immutability:

- Time
- Memory
- Performance with large data

## 7. Other alternative of mutate data / less expensive / 

### Data structures:

#### Trie or digital tree:
https://learnersbucket.com/tutorials/data-structures/trie-data-structure-in-javascript/

Other:
https://immutable-js.com/#the-case-for-immutability


