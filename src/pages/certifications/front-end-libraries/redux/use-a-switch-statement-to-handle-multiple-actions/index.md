---
title: Use a Switch Statement to Handle Multiple Actions
---
## Use a Switch Statement to Handle Multiple Actions

<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->

Tip: Make sure you don't use "break" commands after return statements within the switch cases, unlike for JavaScript. Place "break" only after the "default" switch case

Solution 
````javascript
const authReducer = (state = defaultState, action) => { 
  // change code below this line 
  switch (action.type) { 
    // Do not set action.type equal a condition. if(action.type === 'login'){} works fine but NOT switch(action.type === 'login'){}. The cases specified decide on the response of the switch.
    case 'LOGIN':  
      return { 
        authenticated: true 
      } 
    // Note the lack of 'break;' until after the 'default' case unlike for JavaScript
    case 'LOGOUT': 
      return { 
        authenticated: false 
      } 
    default: 
      return defaultState 
    break; 
  } 
  // change code above this line 
}; 
````
