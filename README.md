# ng-prism

Provides dynamic syntax highlighting for your documentation app using PrismJS and Angular

- Eliminates the need to painfully copy and escape HTML in your code demos
- Can be used with routing libraries such as [UI-Router](https://ui-router.github.io/) 

### Installation

1. `npm install joswhite/ng-prism`

2. `angular.module('myApp', ['ng-prism']);`

3. `<script src="ng-prism.js">`<br>
   `<link rel="stylesheet" href="ng-prism.css">`

### Use

- See examples in `src/index.html`

- `pre > code[highlight="language-xxxx"]` (highlights the code inside it)

    * `highlight` attribute specifies PrismJS language (default: `language-javascript`)
    * HTML markup needs to be escaped

- PrismJS direct use (just like https://prismjs.com)

    * If using a routing library, use `pre > code[highlight]` instead

- `repeat-as-code` attribute (retains HTML element and highlights the code that created it)

    * `repeat-as-code="inner"` highlights the code that created its HTML children elements
    
- `toggle-repeat-code` attribute (`repeat-as-code` with a "Show Code" button)
    
- `toggleable-code` element ("Show Code" button for any code block)

   * child should be any element that produces a code block 
    
### Example App

Run `npm start` and navigate to localhost:8080. 

### Development

`npm install -g gulp`

- Build: `gulp build:development`
- Watch: `gulp`
- Works with LiveReload

### Notes

- Default theme is prism-okaidia. You can change this in `src/main.scss`
- The consuming application is responsible for styling the "Show Code" button
- ng-prism converts 4 spaces to the tab character and forces LTR display on the code block
- This project uses [jedwardhawkins/ng-gulp](https://www.github.com/jedwardhawkins/ng-gulp)
