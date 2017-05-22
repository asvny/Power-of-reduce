# Power-of-reduce

Most of ECMAScript 2015 `Array methods` using `array.reduce`

### Map
```js
const map = (fn,arr) => arr.reduce((arr,curr)=>{
  arr.push(fn(curr));
  return arr;
},[])
```

### Filter
```js
const filter = (fn,arr) => arr.reduce((arr,curr)=>{
  !!fn(curr) ? arr.push(curr) : void 0
  return arr;
},[]);
```

### Some
```js
const some = (fn,arr) =>  arr.reduce((bool,curr)=>{
  return !!fn(curr) || bool ? true : false
},false);
```

### Every
```js
const every = (fn,arr) =>  arr.reduce((bool,curr)=>{
  return !!fn(curr) && bool ? true : false
},true);
```

### Contains
```js
const contains = (val,arr) =>  arr.reduce((bool,curr)=>{
  return curr === val || bool ? true : false ;
},false);
```
