# React Basics
### Definition
React JS is a JavaScript Library for building front end application or user interfaces (UI). It allows us to create reusable UI components. It is the most popular JS front-end framework in use today. It was released by Facebook in 2013 and they still use it today for many of their applications. Manly it is used in three places: web development, mobile app development and desktop app development.
### Setting up
We need text editor and web browser. 

We need NPM- it’s a package manager, it comes with NodeJS, so we need to install NodeJS.

Webpack- module bundler

Babel- toolchain which converts modern codes into compatible version of JS in current and older browsers.
### React JSX
JSX is a syntax extension to JavaScript used in ReactJS that allows writing JavaScript that looks similar to HTML. In other words, it is a kind of templating language but with the power of JavaScript. It makes writing codes easier.
### Components
React is component-based framework. An example of a component could be a form or even just a form field or button on a website. We could build up complete applications using such components by simply nesting them. Components in React can manage their own state and communicate that state to child components. Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML. Components come in two types, Class components and Function components.
### Creating a new react app
There are many steps involved. At first, we need to install NodeJS and then we can start installing React using npm. 
*Create React App* is a tool, built by developers at Facebook that gives us a massive head start when building React app. It saves us from time consuming setup and configuration. We can simply run one command(create-react-app) and it will set up all the tools we need to start a React project.
```
Syntax:
npx create-react-app my-app
cd my-app
npm start
```
# React State and Events
### What is react state?
React component has a built-in state object. By “state” means the data that populates web application. An example would be a user profile form that holds the state of the user’s data, including first name, last name, and other values. 

The state object is initialized in the constructor. It can contain as many properties as we like. We can refer state object anywhere in the component by using the syntax: 

this.state.propertyname

When a value in the state object changes, the component will re-render, meaning that the output will change according to the new value. To change a value in the state object, we use ** this.setState() ** method.
### Demonstration of state in react app
```
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  render() {
    return (
      <div>
        <h1>My {this.state.brand}</h1>
        <p>
          It is a {this.state.color}
          {this.state.model}
          from {this.state.year}.
        </p>
      </div>
    );
  }
}

```
### What is an event?
React can perform actions based on user’s interest which are called as events. React has the same events as HTML: click, change, mouseover, etc.
### How are events handled in react?
React events are written in camelCase syntax. React event handlers are written inside curly braces: onClick = {shoot}
To pass an argument to an event handlers, we use an arrow function. 
### Demonstration of react event
```
function Football() {
  const shoot = () => {
    alert("Great Shot!");
  }

  return (
    <button onClick={shoot}>Take the shot!</button>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Football />);

```
## React hooks and single page web app with react.js
### What are react hooks?
Hooks are new addition to React 16.8. Hooks are functions that let us “hook into” React state and lifecycle features from function components. They let us use state and other React features without writing a class. 

React provides few built-in hooks like useState, useEffect, etc. We can also create our own hooks to reuse stateful behaviour between different components. 

### Demonstration of using hooks
```
import React, { useState } from 'react';
function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

```
### How to build  a single page web application with react.Js?



