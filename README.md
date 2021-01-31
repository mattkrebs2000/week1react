# React Crash Course (TodoList)

This is the code for the Brad Traversy crash course on YouTube. React - Class Components. 
Here is the youtube link:

https://www.youtube.com/watch?v=sBws8MSXN7A&t=2103s

## Quick Start

```bash
# Install dependencies
npm install

# Serve on localhost:3000
npm start

# Build for production
npm run build



Questions on the Code: 


1. For this question consider all of the .js files in the SRC folder and the “imports” (the ones that import another component - FOR example: import Todos from './components/Todos';) that exist at the top of each of these pages:

    a. What do you notice about the system for importing components into another component in React? (In other words) If App.js is a “Parent” component to “Todos.js” a “child” component - Can you make sense of whether or not there is a rule about whether or not “child” components should be imported into “parent” components or the opposite? 

    b. Why do components need to be imported at all? Test this by commenting out an import at the top of App.js. 


2. Go to this link: https://drive.google.com/file/d/1Y2sydLwhY51kPyIXWSRcrypCgfQmYU7Y/view?usp=sharing
    a. Make a copy 
    b. Create a diagram that represents all of the components and the way in which they are connected. 
    c. Using the diagram that was created, figure out the path that the “delTodo” function followed from when it was first created (in App.js) to when it became functional on the application (on the screen). What was its path? In other words which components was it brought into and how did it finally make its way onto the screen as an “x.”
    d. Do the same thing with the state “todos.” In which components did it originate from? Which components was it brought into and how did it finally make its way to impacting what you see on the screen?


3. Look inside the AddTodo.js - notice that there is state (“title”) and two functions (onSubmit, onChange). 

    a. Why is the “title” state inside the AddTodo component but the “todos” state (which is also used in the AddTodo component) is not inside the AddTodo component? 

    b. Why are the two functions “onSubmit” and “onChange” inside the AddTodo component but the “addTodo” function in App.js which is only used by the AddTodo.js component is not inside the AddTodo.js component? 

    c. Do you think that addTodo function in App.js could be taken out of App.js and placed in the AddTodo.js component without interrupting the Apps functionality? 

4. Go to TodoItem.js and notice the following code: 
const { id, title, completed } = this.props.todo;
This is an example of “destructuring.” It is a shortcut taken by the person writing the code. 

    a. Comment this line out
    b. Notice that the code now has some issues
    c. Review the following link: https://medium.com/@lcriswell/destructuring-props-in-react-b1c295005ce0
    d. Try to fix the code so that it works without using the destructuring. 


5. For this question please do the following

    a. Open the console
    b. Clear the console
    c. Refresh the application
        i. What is the output in the console when you refresh the application?
        ii. Where is the code that resulted in this output?
        iii. See link: https://www.w3schools.com/react/react_lifecycle.asp
            1. Be very specific: When did this happen? 

6. For this question please take a look at the following link https://www.w3schools.com/react/react_css.asp
    
    a. Find in the code 3 types of styling
        i. Show and Describe those examples. 


7. Take a look at the functions (markComplete, delTodo, addTodo) in App.js component. Each of them contains an “argument” or a “parameter” that was passed through it (id, id, title - respectively). 

    a. Inside each of those functions curly brackets input for example console.log(“testing1”, id); to see what the “id” is.
    b. What is it? 
    c. How exactly did it get there? 


8. Notice the following: when you “npm start” from inside the folder the application routes to the home page which has a list of “Todos.” When you click on the word “About” from the heading the application routes you to a different display. When you click on the word “Home” the application routes you back to the original display of “Todos.”

    a. Take a look at the “return” section App.js and Header.js
        i. Try to manipulate the code in such a way that when you do a “npm start” the application loads to the “About” section and only goes to the (original) “Home” section with all of the “todos” if you click on the “Home” link.  
    b. Explain what steps were necessary to make the above change. 
    c. What is the word “Exact” used for in App.js. 


9. Comment out the line “e.preventDefault();” and then press the submit button after entering something in the input box. 

    a. How does the behaviour of the application change? 
    b. Take a look at this link: https://www.tutorialspoint.com/stop-making-form-to-reload-a-page-in-javascript
    c. Explain what happens in an application when you have the “preventDefault()” vs. when you don’t.


10. When we cloned this application it had one ternary operator in it. 

    a. If you are unclear on what a ternary operator is look it up. 
    b. Do a search of ternary operators in the application folder. What is it doing? 
    c. Create your own Ternary Operator in which you change the color of the red buttons to blue whenever the todos have been completed. 


11. Explain in regular english what the function below is saying. 

    a. Hint: To fully understand what is happening I recommend taking a look at where in the code the markComplete function is invoked--


markComplete = (id) => {
   this.setState({
     todos: this.state.todos.map((todo) => {
       if (todo.id === id) {
         todo.completed = !todo.completed;
       }
       return todo;
     }),
   });
 };


