# ESLint & Prettier Basic Setup

This setup uses ESLint with Prettier plugin to do linting and formating in one. 

## With VS Code

Use VS Code ESLint package which makes the editor to lint and fix for you.

1. Install [ESLint Package](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
2. Setup some VS Code settings via Code/File → Preferences → Settings.

```json
// Auto-save configs
"editor.formatOnSave": true,
// Turn it off for JS and JSX, we will do this via ESlint
"[javascript]": {
  "editor.formatOnSave": false
},
"[javascriptreact]": {
  "editor.formatOnSave": false
},
// Tell the ESLint plugin to run on save
"eslint.autoFixOnSave": true,
// Optional BUT IMPORTANT: If you have the prettier extension enabled for other languages like CSS and HTML, turn it off for JS since we are doing it through Eslint already
"prettier.disableLanguages": ["javascript", "javascriptreact"],
```