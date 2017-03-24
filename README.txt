windows cmd 
> node -v
v6.9.1
>npm -v
3.10.8
https://angular.io/docs/js/latest/quickstart.html
Here is the file structure:
angular-quickstart
src
app
app.component.js
app.module.js
main.js
index.html
styles.css
============
Let's follow a process that's closer to what we'd do in real life.
    Set up our development environment
    Write the Angular root component for our app
    Add an Angular Module
    Bootstrap it to take control of the main web page
    Write the main page (index.html)
    Add some CSS (styles.css)
1. Add a package.json file to the project folder and copy/paste the following:
2.Install these packages by opening a terminal window (command window in Windows) and running this npm command.
>>>>>>> npm install
3.Our First Angular Component
The Component is the most fundamental of Angular concepts. A component manages a view - a piece of the web page where we display 
information to the user and respond to user feedback.
Technically, a component is a class that controls a view template. We'll write a lot of them as we build Angular apps. 
This is our first attempt so we'll keep it ridiculously simple.
Create an application source sub-folder
We like to keep our application code in a sub-folder off the root called src/app/. 
Execute the following command in the console window.
>>>> mkdir app
>>>> cd    app
Add the component file
Now add a file named app.component.js and paste the following lines:
src/app/app.component.js
4.The Component definition object
ng.core.Component() tells Angular that this class definition object is an Angular component. The configuration object 
passed to the ng.core.Component() method has two fields, a selector and a template.
5.Add an NgModule
Angular apps are composed of Angular Modules that snuggly contain all our components and everything else we need for our app.
Create the src/app/app.module.js file with the following content:
6.Bootstrap it!
Add a new file , main.js, to the src/app/ folder as follows
We need two things to launch the application:
    Angular's platformBrowserDynamic().bootstrapModule function
    The application root module that we just wrote.
7.Add the index.html
Angular displays our application in a specific location on our index.html. It's time to create that file.
There are three noteworthy sections of HTML:
    We load the JavaScript libraries we need; learn about them below.
    We load our JavaScript files.
    We add the <my-app> tag in the <body>. This is where our app live
    8.Configure the server
We're going to use a static server called lite-server that loads index.html in a browser and refreshes the browser when application files change.
The static server will use the bs-config.json file as configuration. This files tells the server that src/ is the base directory to serve, and that any requests to node_modules/ should be routed to node_modules/ in the root directory instead of src/node_modules/
Run!
Open a terminal window and enter this command:
>>>>> npm start
That command runs lite-server.
In a few moments, a browser tab should open and display
Output of quickstart app
Congratulations! We are in business.