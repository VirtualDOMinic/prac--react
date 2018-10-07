# Official intro to react: tic tac toe
Following "[Tutorial: Intro to React](https://reactjs.org/tutorial/tutorial.html)"

Tutorial doesn't assume any existing React knowledge, and involves building a small game: a way to learn fundamental React techniques by "doing"

## Notes
Misc notes taken as I follow the tutorial:
1. Decided to set up local dev environment using `create react app` (`npm i -g create-react-app`)
    1. `create react app tictactoe`
    2. Woo! After `cd`ing inside and `npm start`ing I successfully got the "Welcome to React" page :)
    3. Now time to get rid of what I've been given: `rm -f src/*`
    4. Added `index.css` and `index.js` with their respective boilerplate (or slightly beyond IMO) content
    5. `npm start` successfully loads up the 3x3 table/grid
2. Note: installed `sublime babel` VS Code extension, as per the tutorial's recommendation
3. "React has a few different kinds of components, but we’ll start with React.Component subclasses"
```jsx
  class JobList extends React.Component {
  render() {
    return (
      <div className="work-list">
        <h1>Application List for {this.props.name}</h1>
        <ul>
          <li>Nested</li>
          <li>FAC</li>
          <li>Wellcome</li>
          <li>Himself</li>
        </ul>
      </div>
    );
  }
}
// Example usage: <JobList name="Dom" />
```
4. The above JSX transforms (thanks to Babel) into the less-readable `React.createElement` statements
5. Cool things about react/JSX:
    1. You can put any JS expressions within braces `{ }` in JSX
    2. "Each React element is a JavaScript object that you can store in a variable or pass around in your program."
6. "With `onClick={() => alert('click')}`, we’re passing a function as the onClick prop. It only fires after a click. Forgetting `() =>` and writing `onClick={alert('click')}` is a common mistake, and would fire the alert every time the component re-renders."
7. We give React components state by setting `this.state` in their constructors. This state is private to the React component that it's defined in.
  1. So, inside the `class`, above the `render` function, we could add the constructor and state as such:
```js
constructor(props) {
  super(props);
  this.state = {
    value: null,
  };
} 
```
8. Note: "In JavaScript classes, you need to always call super when defining the constructor of a subclass. All React component classes that have a constructor should start it with a super(props) call."
9. "To collect data from multiple children, or to have two child components communicate with each other, you need to declare the shared state in their parent component instead. The parent component can pass the state back down to the children by using props; this keeps the child components in sync with each other and with the parent component."
10. 