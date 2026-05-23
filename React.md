# React Engineering Notes ⚛️

# What is React?

React is a JavaScript library used for building modern, dynamic, and component-based user interfaces.

Created by:
Meta (Facebook)

React helps developers build scalable frontend applications efficiently.

---

# Why React?

Without React:
- Manual DOM manipulation becomes messy
- Code becomes difficult to maintain
- UI updates become complex

React solves this using:
- Components
- State management
- Virtual DOM
- Reusable UI

---

# Advantages of React

- Reusable components
- Faster UI updates
- Component-based architecture
- Large ecosystem
- Strong community support
- Easy state-driven UI updates

---

# Virtual DOM

React uses:
Virtual DOM

Instead of updating the real DOM directly:
- React creates virtual copy
- Compares changes
- Updates only changed elements

This improves performance.

---

# Creating React App

Using Vite:

```bash
npm create vite@latest
```

Select:
- React
- JavaScript

Install dependencies:

```bash
npm install
```

Run project:

```bash
npm run dev
```

---

# Project Structure

```txt
src/
│
├── App.jsx
├── main.jsx
├── components/
└── assets/
```

---

# JSX

JSX stands for:
JavaScript XML

It allows writing HTML-like syntax inside JavaScript.

Example:

```jsx
function App(){

   return(
      <h1>Hello React</h1>
   );

}
```

---

# JSX Rules

## 1. Return one parent element

Correct:

```jsx
return(
   <div>
      <h1>Hello</h1>
      <p>React</p>
   </div>
)
```

Wrong:

```jsx
return(
   <h1>Hello</h1>
   <p>React</p>
)
```

---

## 2. Use className instead of class

HTML:

```html
class=""
```

React:

```jsx
className=""
```

---

## 3. JavaScript inside JSX uses {}

Example:

```jsx
const name = "Bhargav";

<h1>Hello {name}</h1>
```

---

# Components

Components are reusable UI blocks.

Examples:
- Navbar
- Footer
- Cards
- Sidebar

---

# Functional Component

```jsx
function Navbar(){

   return(
      <h1>Navbar</h1>
   );

}

export default Navbar;
```

---

# Using Components

```jsx
import Navbar from "./Navbar";

function App(){

   return(
      <div>

         <Navbar />

      </div>
   );

}
```

---

# Props

Props are used to pass data between components.

Example:

```jsx
function Student(props){

   return(
      <h1>{props.name}</h1>
   );

}
```

Usage:

```jsx
<Student name="Bhargav" />
```

---

# Destructuring Props

Cleaner approach:

```jsx
function Student({name}){

   return(
      <h1>{name}</h1>
   );

}
```

---

# useState Hook

useState is used to manage dynamic data in React.

Import:

```jsx
import { useState } from "react";
```

---

# Counter Example

```jsx
import { useState } from "react";

function App(){

   const [count, setCount] = useState(0);

   return(
      <div>

         <h1>{count}</h1>

         <button onClick={() => setCount(count + 1)}>
            Increase
         </button>

      </div>
   );

}

export default App;
```

---

# Understanding useState

```jsx
const [count, setCount]
```

- count → current state value
- setCount → updates state

---

# Event Handling

React events use camelCase.

Examples:
- onClick
- onChange

---

# Button Click Example

```jsx
<button onClick={handleClick}>
   Click
</button>
```

Function:

```jsx
function handleClick(){

   console.log("Clicked");

}
```

---

# Form Handling

```jsx
import { useState } from "react";

function App(){

   const [name, setName] = useState("");

   return(
      <div>

         <input
            type="text"
            onChange={(e) => setName(e.target.value)}
         />

         <h1>{name}</h1>

      </div>
   );

}
```

---

# Understanding e.target.value

Used to access current input value.

---

# Conditional Rendering

Used to display UI based on conditions.

Example:

```jsx
{
   isLoggedIn
   ? <h1>Welcome</h1>
   : <h1>Please Login</h1>
}
```

---

# List Rendering

Rendering arrays using map().

Example:

```jsx
const fruits = ["Apple", "Banana", "Mango"];

function App(){

   return(
      <div>

         {
            fruits.map((fruit, index) => (
               <h1 key={index}>{fruit}</h1>
            ))
         }

      </div>
   );

}
```

---

# Why key is Important

React uses keys to track elements efficiently during re-rendering.

---

# React Styling

## Inline Styling

```jsx
<h1 style={{color:"blue"}}>
   Hello
</h1>
```

---

# CSS File Styling

```jsx
import "./App.css";
```

---

# React Folder Structure

Recommended:

```txt
src/
│
├── components/
├── pages/
├── hooks/
├── assets/
├── styles/
└── utils/
```

---

# React Developer Mindset

In React:
UI depends on state.

When state changes:
React automatically updates UI.

No manual DOM manipulation required.

---

# Common Beginner Mistakes

- Forgetting export default
- Wrong import paths
- Missing key in map()
- Directly modifying state
- Returning multiple parent elements
- Using class instead of className

---

# Mini Projects Built

- Counter App
- Todo App
- Notes App
- Weather App
- GitHub Profile Finder

---

# Upcoming Topics

- useEffect()
- API Fetching
- React Router
- Context API
- Custom Hooks
- Authentication
- State Management
- Performance Optimization

---

# Interview Questions

## What is React?

React is a JavaScript library used for building component-based user interfaces.

---

## What is JSX?

JSX is a syntax extension that allows writing HTML-like code inside JavaScript.

---

## What is Virtual DOM?

Virtual DOM is a lightweight copy of the real DOM used by React to optimize UI updates.

---

## What are Props?

Props are used to pass data from parent component to child component.

---

## What is useState?

useState is a React hook used to manage component state.

---

## Difference between Props and State

Props:
- Passed from parent
- Read-only

State:
- Managed inside component
- Dynamic and mutable

---

# Key Takeaway

React makes frontend development:
- scalable
- reusable
- dynamic
- maintainable

using:
- components
- state
- declarative UI
- reusable architecture
```
