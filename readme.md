# What is the expected output of following code?

```
const arr = [1, 2, 3, 4]

arr.map(foo)
arr.map(fooTwo)

function foo(item, index) {
  console.log(`Foo Item: ${index} - ${item}`)
}

const fooTwo = (item, index) => {
  console.log(`FooTwo: ${index} - ${item}`)
}
```

_Ans_

```
Declare Item: 0 - 1
Declare Item: 1 - 2
Declare Item: 2 - 3
Declare Item: 3 - 4
Uncaught ReferenceError: Cannot access 'fooTwo' before initialization
    at Line No:4
(anonymous) @ Line No:4
```

# What will be the output of following code?

```
function MyNumberOperation(n) {
  this.number = n
  this.square = n * n
}

MyNumberOperation.prototype.valueOf = function() {
  return this.number + this.square
}

const object1 = new MyNumberOperation(4)

console.log(object1)
console.log(object1 + 3)
```

_Ans_

```
MyNumberOperation {number: 4, x: 16}
23
```

# What will be the output of following code?

```
const arr = [9, 0, 2, 3, 1]
const res = arr.find(x => {
  console.log(x)
  return x < 2
})
console.log(res)
```

_Ans_

```
9
0
0
```

# What will be the output of following code?

```
const arr = [9, 0, 2, 3, 1]
const res = arr.some(x => {
  console.log(x)
  return x < 2
})
console.log(res)
```

_Ans_

```
9
0
true
```

# What is the difference between following code block?

A)

```
const arr = [9, 1, 2, 8, 2, 3, 1, 0, 3, 7]
const num = 3

const arrFilter = arr.filter(x => {
  console.log(x)
  return x === num
})
console.log(arrFilter)
```

B)

```
const arr = [9, 1, 2, 8, 2, 3, 1, 0, 3, 7]
const num = 3

const arrFind = arr.find(x => {
  console.log(x)
  return x === num
})
console.log(arrFind)
```

_Ans_

A)

```
9
1
2
8
2
3
1
0
3
7

(2) [3, 3]
  0: 3
  1: 3
```

B)

```
9
1
2
8
2
3

3
```
