#React :
------------------------------------------------------------------
- react is library in js
- use syntax extension jsx : javascript xml
-  it allow to write a code js code in xml file 
- it completely component code
- npm : node package manager 
- vite is development server
- installation : 
 => have node.js 
 => npm create vite@latest 
 => npm install 
 => npm run dev : start development server
- now talk about that folder  :
 node_modules : external libraries for are help
 public : contains public assets 
 src : source folder , we'll spend all 99% time in this one 
 src/assets : contain our app assets
 

- rfc => snippet to create a functions
     use folder : components to store components , utils to store js and stuff 
     use import React , { useState } from 'react';  => when I have to show like any button press and somethings happen like dropdown menu or somethings
- I have to create function  with capital later ex Header.jsx => function Header()
- I can write a javascript in {} at an place 
 ex :  <p>&copy; { } Website</p>
-  it's all about reusing component(reusable section of code  )
- -----------------------------------------------
###- how to style with react component :
 1. external
 2. Modules
 3. inline
 => external : 
 .button{
  background-color: hsl(200 , 100% , 50%);
  color:  white;
  border: none;
  cursor: pointer;
  padding: 10px 20px;
  border-radius: 5px;
}
 => module : I have to create a folder for specific component and store that component.module.css file in that too throught that I can use css in my main component.jsx  file.

=> inline : create a variable  
 ex : const style = { color : "white" , border : "none" , }
for using this <button style={style}>click</button>

-------------------------------------------------------------------------

###-props => read - only properties that are shared between components . A parent component can send data to a child component.
-  if I store  other than string value I have to add {} in this 
- 
