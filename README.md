# react-starter

## Follow the steps below to clean-up a new project created with create-react-app
- run `npx create-react-app projectname`
- navigate into the project folder and open the project in vs-code.
- open **index.js**: Remove the import of `serviceWorker` and all code that refers to this file
- remove the file `serviceworker.js`
- open **App.js**: Remove the import of the Logo
- Still in **App.js** remove everything inside the outer div, but leave the div
- Still in **Ap.js** add a h1-tag with a simple text, just to see everything is OK
- Remove the file `logo.svg`
- Remove the file `app.test.js` (We are not going to do client-side testing this semester)


## IMPORTANT! ONLY for the small intro-exercises day1 +2

```
//Create a new file App2.js (and App3.js ....)
//In index.js, delete EVERYTHING BELOW the import of App and use the strategy below to switch between the smaller exercises
//NOTE: THIS IS NOT THE WAY TO DO THINGS AFTER THE FIRST 2-3 DAYS

import App2 from './App2'

let app = <App/>

const DontUseMeForReal = () => {
    return (
        <div className="App" onClick={handleSelect}>
         <a href="/"  id="app1">ex1</a> &nbsp;
         <a href="/"  id="app2">ex2</a> &nbsp;
         {app}
        </div>
    )
}

function handleSelect(event) {
    event.preventDefault();
    const id = event.target.id;
    switch (id) {
        case "app1": app = <App />; break;
        case "app2": app = <App2 />; break;
    }
    ReactDOM.render(<DontUseMeForReal />, document.getElementById('root'));
}

ReactDOM.render(<DontUseMeForReal />, document.getElementById('root'));
```
