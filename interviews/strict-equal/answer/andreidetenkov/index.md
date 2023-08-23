---
related:
  -- js/typecasting
keywords:
  - операторы сравнения, приведение типов
---


Операторы `==` и `===` в JavaScript — это операторы сравнения, которые мы используем, чтобы определить, равны или нет два значения.

Двойное равно `==` часто называют «нестрогим равенством», потому что этот оператор перед сравнением величин выполняет приведение типов:

```js
const foo = 100;
const bar = '100';
console.log(foo == bar) // true
```

---
Оператор `===` выполняет строгое сравнение, без приведения типов. 
При использовании тройного равно сравниваются и типы, и значения.

При сравнении переменных сначала проверяется, отличаются ли их типы. 
Если типы совпадают, то проверяется значение. Если значения одинаковы, возвращается true.

```js
const foo = 100;
const bar = '100';
console.log(foo === bar); // false

const foo = '100';
const bar = '100';
console.log(foo === bar); // true
```

---
Преобразование типов в JavaScript иногда может приводить к неожиданным результатам, 
поэтому хорошей практикой считается использовать оператор строгого равенства `===` при сравнении.