# Boostraping React Part 1 and Part 2

## Part 1

[Video](https://vimeo.com/928144595/b8c9449742?share=copy)

This guide walks you through the steps of setting up a new React application, running it, and making initial modifications using Visual Studio Code as the IDE. The steps include using the command-line interface to create a new React application, launching it, and then making initial clean-up in the project structure.

### Step 1: Creating a New React Application
Use the `create-react-app` tool to bootstrap a new React application. In your command line, navigate to the directory where you want your project to reside and execute the following command:

```bash
npx create-react-app first-project
```

This command creates a new React application named "first-project" in the specified directory. The process may take a few minutes as it sets up the necessary files and dependencies for a functional React app.

### Step 2: Starting the Development Server
Once the setup is complete, navigate into your project's directory:

```bash
cd first-project
```

Then, start the development server to see your new React application in action:

```bash
npm start
```

This command launches the app in your default web browser, displaying the default React app page.

### Step 3: Opening the Project in Visual Studio Code
To open your project in Visual Studio Code, you can use the `code` command followed by a period:

```bash
code .
```

This command opens your current project directory in Visual Studio Code, allowing you to edit and explore your new React application.

### Step 4: Exploring the Project Structure
The new React application comes with a predefined structure, including a `public` directory containing the `index.html` file and a `src` directory with the React source files.

- `public/index.html`: This is the main HTML file where your React app will be rendered. It contains a `div` with an id of `root`, which is the mounting point for your React application.
- `src/index.js`: This file attaches your React app to the `index.html` file, targeting the `div` with the id of `root`.
- `src/App.js`: This file contains the main `App` component, which is rendered inside the `div` with the id of `root` in the `index.html` file.

### Step 5: Cleaning Up the Default Project
You might want to clean up some of the default files and code that come with the `create-react-app` setup:

1. In `src/index.js`, you can remove unnecessary imports and code, such as `reportWebVitals`.
2. In `src/App.js`, you can simplify the `App` component by removing the default content and adding a simple "Hello World" message:

```javascript
import './App.css';

function App() {
  return (
    <div className="App">
      <h1>Hello World</h1>
    </div>
  );
}

export default App;
```

3. In `src/App.css`, you can clear out or modify the default styles as needed.

After making these changes, save your files. Your React app will automatically reload in the browser, reflecting your updates.

### Conclusion
This guide has shown you how to create a new React application, run it, and make initial adjustments to the project structure. You're now ready to start building your React application by adding new components, styling, and functionality as needed.

## Part 2

[Video](https://vimeo.com/928149499/7be76f4b4e?share=copy)

This guide provides an overview of the initial structure and setup of a React application created using the `create-react-app` tool. It explains the purpose of different files and directories, and how to make simple modifications to your React app.

### Understanding the Project Structure

#### Public and Source Directories
- **Public Directory**: Contains files that do not need to be compiled by React, such as the `favicon.ico` and the `index.html`. This directory holds static assets.
  
  - **`index.html`**: Serves as the template for your React application. It contains a `div` with an `id="root"`, which is the mounting point for your React app. Normally, you won't need to make many changes to this file, except possibly changing the title of your app within the `<title>` tag.

    ```html
    <title>My First React App</title>
    ```

- **Source (SRC) Directory**: Contains all the React components, styles, and JavaScript files that will be compiled by React.

#### Index.js and App.js
- **`index.js`**: The entry point for the React application. It imports the necessary React modules and the root app component. It uses `ReactDOM` to render the `App` component into the `div` with `id="root"` in `index.html`.

  ```javascript
  import React from 'react';
  import ReactDOM from 'react-dom/client';
  import './index.css';
  import App from './App';

  const root = ReactDOM.createRoot(document.getElementById('root'));
  root.render(
    <React.StrictMode>
      <App />
    </React.StrictMode>
  );
  ```

- **`App.js`**: Contains the main `App` component of your React application. Initially, it might include some placeholder content that you can replace with your own. For example, to display "Hello Everyone", you might have:

  ```javascript
  import './App.css';

  function App() {
    return (
      <div className="App">
        <h1>Hello Everyone</h1>
      </div>
    );
  }

  export default App;
  ```

### Making Simple Modifications

1. **Changing the App Title**: In the `public/index.html` file, change the content of the `<title>` tag to update the title that appears in the browser tab.

2. **Cleaning up the `public` Directory**: Remove unnecessary icons or files that were included by default but are not needed for your project.

3. **Updating the `App` Component**: In `src/App.js`, you can start by removing any import statements that are not used (e.g., logo images) and simplify the component to display a simple message like "Hello Everyone". You can also clear out or adjust the `src/App.css` file to tailor the styling of your app component.

4. **Understanding React Components**: In React, components that are custom or user-defined should start with an uppercase letter (e.g., `App`), while standard HTML elements within JSX code are written in lowercase (e.g., `div`, `h1`).

By following these steps, you will have a clean slate to start developing your React application with a better understanding of its structure and the role of different files.

