0x05. React state
Front-end
JavaScript
ES6
React
 Weight: 1
 Project will start Jul 10, 2024 6:00 AM, must end by Jul 16, 2024 6:00 AM
 Checker was released at Jul 11, 2024 6:00 PM
 Manual QA review must be done (request it when you are done with the project)
 An auto review will be launched at the deadline


Resources
Read or watch:

State and lifecycle
SetState and State callback
Context
Forms and Controlled components
Lifting State Up
React Hooks
Enzyme State
Enzyme SetState
Enzyme Instance
Enzyme Simulate
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

What the state of a component or a container is
The lifecycle of a component
How to modify a state and execute code in the right order
What a controlled component is
How to use Forms in React
How to reuse smaller components, keep them pure, and lift its state to principal containers
The use of a React Hook and how to create one
How to test State changes with Enzyme
Requirements
All your files will be interpreted/compiled on Ubuntu 18.04 LTS using node 12.x.x and npm 6.x.x
Allowed editors: vi, vim, emacs, Visual Studio Code
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
Tasks
0. Adding a local state for notifications
mandatory
Using the previous project (0x05. React inline styling), we have modularized our React application without worrying about interactions and state, which is usually a recommended process of development. Now, our application is in a good place to start adding logic and state.

Modify the App component in task_0/dashboard/src/App.App.js:

Create a local state to store a displayDrawer element:

Define the default state for the state in the constructor of the Class
Create a function named handleDisplayDrawer that will change the value of displayDrawer to true
Create a function named handleHideDrawer that will change the value of displayDrawer to false
Modify the Notifications import in task_0/dashboard/src/App/App.js:

Pass to the component the prop displayDrawer using the local state
Pass the new functions handleDisplayDrawer and handleHideDrawer
Modify the App test suite in task_0/dashboard/src/App/App.test.js:

Add a test to verify that the default state for displayDrawer is false. Verify that after calling handleDisplayDrawer, the state should now be true
Add a test to verify that after calling handleHideDrawer, the state is updated to be false
Modify the Notifications component in task_0/dashboard/src/Notifications/Notifications.js:

Define the propTypes and the defaultProps for the new props
When clicking on Your notifications, call handleDisplayDrawer
When clicking on the close button, call handleHideDrawer
At this point, after reloading the app, you should be able to show / hide the notifications panel

Modify the Notifications test suite in task_0/dashboard/src/Notifications/Notifications.test.js:

Add a test to verify that clicking on the menu item calls handleDisplayDrawer
Add a test to verify that clicking on the button calls handleHideDrawer
Tips:

Remember that you implemented shouldComponentUpdate. You will need to modify the logic to allow the component to rerender when the prop displayDrawer changes
Use setState and instance when creating tests with Enzyme
Remember to use spies to verify if a function is being called. You can pass a spy as a property
Requirements:

Do not forget to bind the functions you are passing to the children to improve performances
When running, there should not be any lint error in the consol
