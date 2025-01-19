# React Basics

## Overview
React is a **JavaScript library** that uses the **JSX (JavaScript XML)** syntax extension. JSX allows developers to write JavaScript code in an XML-like syntax. React is built entirely on the concept of components, enabling reusable, modular code.

## Key Concepts

### Installation
1. **Prerequisites:** Install Node.js.
2. **Setup with Vite:**
   - Run: `npm create vite@latest`
   - Install dependencies: `npm install`
   - Start the development server: `npm run dev`

### Project Structure
- **node_modules:** Contains external libraries.
- **public:** Contains public assets.
- **src:** The source folder where most development happens (~99% of time spent here).
  - **src/assets:** Stores application assets like images and other media files.
  - **src/components:** Contains React components.
  - **src/utils:** Stores utility JavaScript files.

### Snippets
- Use `rfc` snippet to quickly create functional components.

### Writing Components
1. Components should have their function names start with an uppercase letter. Example:
   ```jsx
   // File: Header.jsx
   function Header() {
       return <h1>Welcome to the Website</h1>;
   }
   ```
2. You can embed JavaScript within JSX using curly braces `{}`. Example:
   ```jsx
   <p>&copy; {new Date().getFullYear()} Website</p>
   ```
3. React focuses on creating reusable components (reusable sections of code).

## Styling React Components

### Methods
1. **External CSS**
   - Write styles in a separate `.css` file and import it into the component.
   - Example:
     ```css
     /* styles.css */
     .button {
         background-color: hsl(200, 100%, 50%);
         color: white;
         border: none;
         cursor: pointer;
         padding: 10px 20px;
         border-radius: 5px;
     }
     ```
     ```jsx
     // File: Button.jsx
     import './styles.css';
     function Button() {
         return <button className="button">Click</button>;
     }
     ```

2. **CSS Modules**
   - Create a module CSS file specific to a component. 
   - Example:
     ```css
     /* Button.module.css */
     .button {
         background-color: hsl(200, 100%, 50%);
         color: white;
     }
     ```
     ```jsx
     import styles from './Button.module.css';
     function Button() {
         return <button className={styles.button}>Click</button>;
     }
     ```

3. **Inline Styles**
   - Use a style object directly in the JSX.
   - Example:
     ```jsx
     const style = {
         color: 'white',
         border: 'none'
     };
     function Button() {
         return <button style={style}>Click</button>;
     }
     ```

## Props
- Props are **read-only properties** shared between components. A parent component can pass data to a child component using props.
- Non-string values in props should be enclosed in curly braces `{}`.
- Example:
  ```jsx
  function Greeting({ name }) {
      return <h1>Hello, {name}!</h1>;
  }

  function App() {
      return <Greeting name="John" />;
  }
  ```

- For Boolean props, use ternary operators to render different UI elements, as booleans themselves aren’t displayed.

---
This document provides an introduction to React basics, including project setup, components, styling, and props.

