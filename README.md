This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).
# JSON Forms VueJS seed App
This seed demonstrates how to use [JSON Forms](https://jsonforms.io) with React 
in order to render a simple form for displaying a task entity.
 
It is based on create-vue-app and only contains minor modifications.

 * Execute `npm ci` to install the prerequisites. If you want to have the latest released versions use `npm install`.
 * Execute `npm start` to start the application.
 
 Browse to http://localhost:3000 to see the application in action.

## File Structure
Let's briefly have a look at the most important files:
* `src/schema.json` contains the JSON schema (also referred to as 'data schema')
* `src/uischema.json` contains the UI schema
* `src/index.js` is the entry point of the application and sets up the redux store 
  that contains the data, the JSON and the UI schema necessary for JSON Forms.
* `src/App.js` is the main React component and makes use of the JSON Forms Component
  in order to render a form.
  
The [data schema](https://github.com/icidel/jsonforms-vuejs-seed/blob/master/src/schema.json) defines   
the structure of a Task: it contains attributes such as title, description, due date and so on.

The [corresponding UI schema](https://github.com/icidel/jsonforms-vuejs-seed/blob/master/src/uischema.json) 
specifies controls for each property and puts them into a vertical layout that in turn contains two
horizontal layouts.

Both the data schema and the UI schema are imported within `index.js`.

## Rendering our form
The `App` component is responsible for rendering our actual form.
It does so by associating JSON schema to VueJS components accorsing to the expected data type (work in progress).

## Custom renderers
Please see [React custom renderer tutorial](https://jsonforms.io/docs/custom-renderers) on how to add custom renderers, but use VueJS components instead (see https://blog.rangle.io/how-to-create-data-driven-user-interfaces-in-vue/ for a simple VueJS generated form sample).
