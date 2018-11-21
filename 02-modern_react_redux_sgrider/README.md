# Following "Modern React with Redux [2019 Update]
Udemy course by Stephen Grider
Much of the notes below will be rough and non-comprehensive. Purely for my own use/to jog my own memory

## My aims
* Solidify my knowledge of the basics of React (i.e. much of the earlier content and notes will be going over concepts I already know and have used)
* Fill in any gaps in my knowledge of the fundamentals
* Get a taste of Redux!

## Progress
- [X] S1: "Let's Dive In!" - CRA, JS Modules, Components
- [X] S2: JSX
- [ ] S3: Props
- [ ] S4: Structuring apps with class-based components
- [ ] S5: State in React components
- [ ] S6: Lifecycle methods
- [ ] S7: User input with forms and events
- [ ] S8: API requests
- [ ] S9: Building lists of records
- [ ] S10: `Ref`s for DOM access
- [ ] S11: Test!
- [ ] S12: Redux intro
- [ ] S13: Integrating React with Redux
- [ ] S14: Async actions with Redux Thunk
- [ ] S15: Redux store design

## Rough notes:
### S1: Intro and CRA (videos 1-10)
* `npm install -g create-react-app`
* `create-react-app [project name]`
    * Can also use `npx create-react-app [project name]`, without having to go through the npm install process
    * `npx` isn't included with older versions of npm
* CRA installs (sets up) Webpack, Babel and a dev server for our project behind the scenes for us!
* Project directory layout:
    * `src`: where we put our source code
    * `public`: folder for static files, e.g. images
    * `node_modules`, `package.json`, `package-lock.json`, `README.md`, `.gitignore`...
* Inside `index.js` we need to:
    * `import React from 'react'`
    * `import ReactDOM from 'react-dom'`
    * `import` syntax is ES2015, `require` syntax is commonJS
* React components
    * They are functions or classes
    * Purpose:
        * Produce HTML to show the user (using JSX)
        * Handle feedback from user, using event handlers

```jsx 
const App = () => {
    return <div>This is a div</div>;
};

ReactDOM.render(
    <App />,
    document.getElementById("root")
    // or document.querySelector("#root")
);
```

### S2: JSX (videos 11-20)
* [Babel have a great repl for looking at how your code is transpiled](https://babeljs.io/repl)
    * Ensure the `React` box is ticked on the left-hand panel
* JSX is very similar to HTML, but has some differences
    * Inline styling:
        * Styling should be in an object, not a string. 
        * Any CSS that uses a dash should be in `camelCase` instead (e.g. `background-color` becomes `backgroundColor`)
        * E.g. `<div style="background-color:red;"></div>` in HTML should be represented as `<div style={{backgroundColor: "red"}}></div>` in JSX
        * Another valid JSX example: `<div style={{border: "1px solid red"}}></div>`
    * class vs className
        * `className` should be used instead of `class` (although this may change in the very near future!)
    * Forbidden property names
        * E.g. `for` shoult be `htmlFor`
    * Referencing JS variables:
        * JS variables can be referenced inside `{curly braces}`
        * See below for exceptions...
* Values JSX can't show
    * Objects! "Not valid as a React child" - cannot reference a whole object inside of JSX where we'd use text




