# React.js

## What it is:
React is a JavaScript library designed for creating user interfaces for single-page web applications. *It's the V in MVC*

## Key Concepts:

### Logic in the Look.

Simply express how your app should look at any given point in time, and React will automatically manage all UI updates when your underlying data changes.

Rather than separate "templates" and "display logic", React is written in a proprietary JSX language - a hybrid of Javascript and HTML. By combining the two, each component written in JSX can be considered a function that takes in data, creates a JavaScript object using HTML syntax, and renders HTML.

```
var MyComponent = React.createClass({/*...*/});
var myElement = <MyComponent someProperty={true} />;
React.render(myElement, document.getElementById('example'));
```

To paint to the page, JSX is transformed into vanilla JS which is then interpreted by the browser as any JS interacting with the DOM would be interpreted.


### Modular, composable components.

The only thing you do is build components. Since they're so encapsulated, components make code reuse, testing, and separation of concerns easy.

It's important to think about each component the same way you would a new function or object: a component should ideally do one thing.

Build components that reuse other components and pass data data from parent to child.

### One-way data flow down the component hierarchy.

When the data changes, React conceptually hits the "refresh" button, and knows to only update the changed parts.

A common pattern is to create several stateless components that just render data, and have a stateful component above them in the hierarchy that passes its state to its children via props. 

The stateful component encapsulates all of the interaction logic, while the stateless components take care of rendering data in a declarative way.




