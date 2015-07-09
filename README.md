# React.js Walkthrough

React is a JavaScript library designed for creating user interfaces for single-page web applications. *It's the V in MVC*

[Topline Overview, on gDrive](https://docs.google.com/presentation/d/1sGJdAk45a4lO1E-y0poEOOHI8ldN1zvMM28eRpa-uMg/edit?usp=sharing)

## Key Concepts:

### Logic in the Look.

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

Build components that reuse other components and pass data from parent to child.


### One-way data flow down the component hierarchy.

When the data changes, React conceptually hits the "refresh" button, and knows to only update the changed parts.

A common pattern is to create several stateless components that just render data, and have a stateful component above them in the hierarchy that passes its state to its children via props. 

The stateful component encapsulates all of the interaction logic, while the stateless components take care of rendering data in a declarative way.


### Simple updates

Express how your app should look at any given point in time, and React will automatically manage all UI updates when your underlying data changes.

When your component is first initialized, the render method is called, generating a lightweight representation of your view. 

When your data changes, the render method is called again. In order to perform updates as efficiently as possible, React diffs (compares) the return value from the previous call to render with the new one, and generates a minimal set of changes to be applied to the DOM.


##### Written by: [Michael](https://github.com/michaelsdennis4), [Fernanda](https://github.com/fcorrea16), & [Ryan](https://github.com/ryaneburke)




