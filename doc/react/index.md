# React Hooks

📌 What exactly hooks are?
 
 We can consider hooks as a JavaScript functions which takes some parameter and return something accordingly. But they servers some complex functionality like managining state and other React features

 📌 Hooks are backwards-compatible

Backwards compatiblity is the characterstic of a technology that allows for  for interoperability with an older legacy system. Hence hooks don’t contain any breaking changes.

 📌 Did Hooks make any changes?

React concepts are same irrelevant of class component or functional component. Hooks can make the code shorter and they provide a quick and efficient way to combine state, props. lifecycle etc...

 📌 Some points to consider while working with hooks

- Don’t call Hooks inside loops, conditions, or nested functions

- Call hooks from React function components

Let's see what a hook looks like

Introduction to widely used React hook - useState

While working with any React hooks, first thing we need to do is to import it.

```js
import { useState } from 'react';
```

useState hook take a parameter as inital value of state and return an array having two values

- the first value is the current state
- the second value is the function that allow us to change our state

Let me show you the return value by printing it out on console 👇

```jsx

import { useState } from 'react';

function UseState() {

  const returnValue = useState(0);
  console.log(returnValue);

  return (
    <div>
      <h1>useState Hook</h1>
    </div>
  )
}
```

You can see the syntax of hooks are quite similar than typical function in React. We just need to pass the parameters according to the acceptance of particular hook.

Moving forward, lets destruct the return value

`const [currentState, setCurrentState] = useState(0);`

- currentState is the value of our current state
- setCurrentState is the function using which we can change current state

```jsx
import { useState } from 'react';

function UseState() {

  const [currentState, setCurentState] = useState(0);

  return (
    <div>
      <h1>useState Hook</h1>
    </div>
  )
}

export default UseState;
```

Let's build a simple counter so that we can understand it effectively. Though, useState has a very powerful use from the small counters to handling the large forms

Basic boilerplate code for counter

```jsx
import { useState } from 'react';

function UseState() {

  const [currentState, setCurentState] = useState(0);

  return (
    <div>
      <h1>{ currentState }</h1>
      <button>PLUS</button>
      <button>MINUS</button>
    </div>
  )
}

export default UseState;
```

Now we want to increase our counter by one by user clicks on the "PLUS" button and decrease the value by one when user clicks on the "MINUS" button

Here value/counter is nothing but our current state which we want to change accordingly.

Here setCurrentState function comes into play

- We will write a handlePlusButton function in order to increase the counter by 1 every time user click plus button

This is pretty easy just call the setCurrentState function and increase counter value just like this

