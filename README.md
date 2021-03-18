# React Tutorial

[link](https://reactjs.org/tutorial/tutorial.html#what-are-we-building)

## Tic-Tae-Toe with React

---

### 1. Set up the app

```shell
npx create-react-app tic-tac-toe
```

---

**Note: Components**

- Small and isolated pieces of code to compose complex UIs
- Components are used to tell React what to expect on the screen. When data changes, React will efficiently update and re-render the components.
- parameters = props (short for “properties”)
- render method ~= return

- sample code:

```JavaScript
class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>
        <ul>
          <li>Instagram</li>
          <li>WhatsApp</li>
          <li>Oculus</li>
        </ul>
      </div>
    );
  }
}

// Example usage: <ShoppingList name="Mark" />
```

**Note: JSX**

- special syntax in React
- "Javascript" + "XML
- example:

```JavaScript
<div example />
```

### 2. Passing Data Through Props

example

```JavaScript
class Board extends React.Component {
  renderSquare(i) {
    return <Square value={i} />;
  }
}
```

`value` is the prop being passed

```JavaScript
class Square extends React.Component {
  render() {
    return (
      <button className="square">
        {this.props.value}
      </button>
    );
  }
}
```

### 3. Making an Interactive Component

`To “remember” things, components use state.`

- add a constructor to the class to initialize the state

```Javascript
class Square extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: null,
    };
  }

  render() {
    return (
      <button
        className="square"
        onClick={() => this.setState({value: 'X'})}
      >
        {this.state.value}
      </button>
    );
  }
}
```

- Note: In JavaScript classes, you need to always call super when defining the constructor of a subclass. All React component classes that have a constructor should start with a super(props) call.
