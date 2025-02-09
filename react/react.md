# React.js Cheat Sheet 📌

## 1️⃣ Basic Setup ⚛️
### Install React
```sh
npx create-react-app my-app
cd my-app
npm start
```

### Import React
```jsx
import React from 'react';
import ReactDOM from 'react-dom';
```

---

## 2️⃣ JSX Syntax 📝
| Feature  | Example |
|----------|---------|
| Variables | `{name}` |
| Expressions | `{2 + 2}` |
| Attributes | `<img src={imageURL} />` |
| Fragments | `<>...</>` |

**Example:**
```jsx
const name = "React";
return <h1>Hello, {name}!</h1>;
```

---

## 3️⃣ Components 🏗️
### Functional Component
```jsx
function Welcome() {
  return <h1>Welcome to React!</h1>;
}
```

### Class Component
```jsx
class Welcome extends React.Component {
  render() {
    return <h1>Welcome to React!</h1>;
  }
}
```

---

## 4️⃣ Props 📦
```jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

<Greeting name="John" />
```

---

## 5️⃣ State Management 🎛️
### Using `useState` Hook
```jsx
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

---

## 6️⃣ Event Handling 🎯
```jsx
function ButtonClick() {
  function handleClick() {
    alert('Button Clicked!');
  }

  return <button onClick={handleClick}>Click Me</button>;
}
```

---

## 7️⃣ Conditional Rendering 🛤️
```jsx
function UserGreeting(props) {
  return props.isLoggedIn ? <h1>Welcome back!</h1> : <h1>Please sign in.</h1>;
}
```

---

## 8️⃣ Lists & Keys 🔑
```jsx
const items = ['Apple', 'Banana', 'Cherry'];

function ItemList() {
  return (
    <ul>
      {items.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  );
}
```

---

## 9️⃣ useEffect Hook 🔄
```jsx
import { useEffect, useState } from 'react';

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    const interval = setInterval(() => setCount(c => c + 1), 1000);
    return () => clearInterval(interval);
  }, []);

  return <p>Time: {count}s</p>;
}
```

---

## 🔟 Forms & Inputs ✍️
```jsx
function Form() {
  const [input, setInput] = useState('');

  return (
    <form>
      <input type="text" value={input} onChange={(e) => setInput(e.target.value)} />
      <p>Typed: {input}</p>
    </form>
  );
}
```

---

# 🚀 Advanced React

## 1️⃣ React Router 🌍
### Install React Router
```sh
npm install react-router-dom
```

### Basic Routing
```jsx
import { BrowserRouter as Router, Route, Routes, Link } from 'react-router-dom';

function Home() {
  return <h1>Home Page</h1>;
}

function About() {
  return <h1>About Page</h1>;
}

function App() {
  return (
    <Router>
      <nav>
        <Link to="/">Home</Link>
        <Link to="/about">About</Link>
      </nav>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </Router>
  );
}
```

---

## 2️⃣ Context API 🎛️ (Global State Management)
```jsx
import { createContext, useContext, useState } from 'react';

const ThemeContext = createContext();

function ThemeProvider({ children }) {
  const [theme, setTheme] = useState('light');
  return (
    <ThemeContext.Provider value={{ theme, setTheme }}>
      {children}
    </ThemeContext.Provider>
  );
}

function ThemeToggler() {
  const { theme, setTheme } = useContext(ThemeContext);
  return <button onClick={() => setTheme(theme === 'light' ? 'dark' : 'light')}>Toggle Theme</button>;
}
```

---

## 3️⃣ Lazy Loading & Code Splitting 📦
```jsx
import React, { lazy, Suspense } from 'react';

const LazyComponent = lazy(() => import('./LazyComponent'));

function App() {
  return (
    <Suspense fallback={<div>Loading...</div>}>
      <LazyComponent />
    </Suspense>
  );
}
```

---

## 4️⃣ Performance Optimization 🚀
### Memoization with `useMemo`
```jsx
import { useMemo, useState } from 'react';

function ExpensiveCalculation({ num }) {
  const computedValue = useMemo(() => {
    console.log("Calculating...");
    return num * 2;
  }, [num]);

  return <p>Computed Value: {computedValue}</p>;
}
```

### Avoid Unnecessary Renders with `React.memo`
```jsx
import React from 'react';

const MemoizedComponent = React.memo(({ value }) => {
  console.log("Rendering...");
  return <p>{value}</p>;
});
