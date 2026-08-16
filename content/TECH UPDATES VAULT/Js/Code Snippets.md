#### Async / Await
```js
async function getValue() {
  return 42;
}
const result = getValue();
console.log(result);
```

An async function always returns a Promise, even if you 'return' a plain value inside it. The value is wrapped. Calling getValue() gives you Promise { 42 }, not 42 directly. You'd need await getValue() or .then() to unwrap it.