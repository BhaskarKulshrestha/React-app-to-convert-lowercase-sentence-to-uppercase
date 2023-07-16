# Documentation For React

# NPX and NPM
```
NPX stands for Node Package eXecute. It is simply an NPM package runner. It allows developers to execute any Javascript Package available on the NPM registry without even installing it. NPX is installed automatically with NPM version 5.2. 0 and above.
```

## Create React App
```
Create React App is a comfortable environment for learning React, and is the best way to start building a new single-page application in React.

It sets up your development environment so that you can use the latest JavaScript features, provides a nice developer experience, and optimizes your app for production. You’ll need to have Node >= 14.0.0 and npm >= 5.6 on your machine. To create a project, run:
```
```.js
npx create-react-app my-app
cd my-app
npm start
```
    
## "use strict";
    Defines that JavaScript code should be executed in "strict mode".

## JSX in React
    JSX stands for JavaScript XML.
    JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement()  and/or appendChild() methods.

    JSX converts HTML tags into react elements.

## What is webpack and why use it?
    Webpack is a static module bundler for JavaScript applications — it takes all the code from your application and makes it usable in a web browser. Modules are reusable chunks of code built from your app's JavaScript, node_modules, images, and the CSS styles which are packaged to be easily used in your website.

## Diffrence between single page application and multi-page application

### Single Page Application :

[Breif explanation of Single page and Multipage Application](https://medium.com/@NeotericEU/single-page-application-vs-multiple-page-application-2591588efe58)
```
A single-page application is an app that works inside a browser and does not require page reloading during use. You are using this type of applications every day. These are, for instance: Gmail, Google Maps, Facebook or GitHub. It is just one web page that you visit which then loads all other content using JavaScript — which they heavily depend on.
```

### Multi Page Allication :
```
Multiple-page applications work in a “traditional” way. Every change eg. display the data or submit data back to server requests rendering a new page from the server in the browser. These applications are large, bigger than SPAs because they need to be. Due to the amount of content, these applications have many levels of UI. 
```
----------------------------------------------------------------

##  NOTE:
```
Some HTML tags are not self closing like "<input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">" so during npm start it will give error 

so to resolve this issue just apply "/" at the end of the tag "<input class="form-control me-2" type="search" placeholder="Search" aria-label="Search" />"
```

----------------------------------------------------------------

## Props in React
```
In ReactJS, the props are a type of object where the value of attributes of a tag is stored. The word “props” implies “properties”, and its working functionality is quite similar to HTML attributes. Basically, these props components are read-only components.Props are used to store data that can be accessed by the children of a React component. They are part of the concept of reusability
```
```.js

<Navbar title="TextUtils" about="About textutils" />
the above code can be used for:example:
<a class="nav-link" href="/">{props.about}

This is called as Prop
```
[Documentation for Props](https://legacy.reactjs.org/docs/components-and-props.html)

## NOTE : While making a component always name the first letter of the file as capital

----------------------------------------------------

```
Navbar.propTypes = {title: PropTypes.string,
                    aboutText:PropTypes.string
}
```
This helps not to make an error while passing the name , if we pass a number to it it will give the error,it only accepts the string value

----------------------------------------------------------

```
Navbar.defaultProps = {
    title : "Set title here",
    aboutText : "Set about here"
}
```
this helps in the condition when user forgets to pass the value.

----------------------------------------------------------------

## isrequired:
```
title: PropTypes.string.isRequired
```
This helps when certain feild is important to be present
### ERROR: act-jsx-dev-runtime.development.js:87 Warning: Failed prop type: The prop `title` is marked as required in `Navbar`, but its value is `undefined`.
 
## State Handling in React

    here we use the concept of Hooks

```
Hooks let you use different React features from your components.
You can either use the built-in Hooks or combine them to build your own.
```
## State Hooks 

State lets a component “remember” information like user input. For example, a form component can use state to store the input value, while an image gallery component can use state to store the selected image index.

To add state to a component, use one of these Hooks:

useState declares a state variable that you can update directly.
useReducer declares a state variable with the update logic inside a reducer function.

```
function ImageGallery() {
  const [i1, i2] = useState(0);
}

NOTE:
we use the i1 to store the value
i2 is used to only update the values of i1 
and i1 can only e updated by i2 via FUNCTION only 
```
