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
