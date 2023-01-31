### Class Component and State

Functional Components
Class Components

# Functional Components
These are JavaScript functions that take props as a parameter if necessary and return react element (JSX).

# Class Components
These components are built using an ES6 class.

# extends
The extends keyword is used to inherit methods and properties from the React.Component.

# render()
The render() method is the only required method in a class component. It returns the JSX element.

# Syntax:

import { Component } from "react";

class MyComponent extends Component {
  render() {
    return JSX;
  }
} 

# React Events
Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

1.React events are named using camelCase, rather than lowercase.
2.With JSX, you pass a function as the event handler rather than a string.

# Eg:
<button onClick={activateLasers}>Activate Lasers</button>
------------------------------------------------------------------------

class MyComponent extends Component {
  handleClick = () => {
    console.log(this)  // MyComponent {...}
  }
  render() {
    return <button onClick={this.handleClick}>Click Me</button>
  }
}
------------------------------------------------------------------------

# State

The state is a JS object in which we store the component's data that changes over time.

When the state object changes, the component re-renders.

# Intialising State:

class Counter extends Component {
  state = { count: 0 }
  render() {
    const { count } = this.state;
    return <p className="count">{count}</p>;
  }
}
------------------------------------------------------------------------

# Updating State

We can update the state by using setState(). We can provide function/object as an argument to set the state

# syntax:
this.setState( prevState => ({... }) )
------------------------------------------------------------------------

onIncrement = () => {
  this.setState((prevState) =>
    console.log(`previous state value ${prevState.count}`)
  )
}
------------------------------------------------------------------------

#  Functional Components vs Class Components

1.Renders the UI based on props
2.Renders the UI based on props and state.


# publish
# https://saieCounterapp.ccbp.tech

