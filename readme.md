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