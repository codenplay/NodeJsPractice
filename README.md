# Node.js Practice


### Update Node Windows

**Update npm**
> npm install npm@latest -g

**Clear npm cache**
> npm cache clean -f

**Install n**
> npm install -g n

**Update node to latest version**
> n latest



### Install and Update Yarn Windows

**Install yarn**
> npm install -g yarn

**Update yarn**
> yarn set version lates


## VS Code Editor Setup

### Extensions

Install the below extensions:  
- ESLint
* Prettier
+ Path Autocomplete


**Settings**  
Go to your Visual Stuido Code settings.json file and add the below settings there:

// config related to code formatting

"editor.defaultFormatter": "esbenp.prettier-vscode",  
"editor.formatOnSave": true,  
"[javascript]": {  
  "editor.formatOnSave": false,  
  "editor.defaultFormatter": null  
},  
"editor.codeActionsOnSave": {  
  "source.fixAll.eslint": true,  
  "source.organizeImports": true  
},  
"eslint.alwaysShowStatus": true  

VS-code terminal set to Git Bash add the below line in Setting.json file 
> "terminal.integrated.defaultProfile.windows": "Git Bash"


**Set Line Breaks**  
Make sure in your VS Code Editor, "LF" is selected as line feed instead of CRLF (Carriage return and line feed). To do that, just click LF/CRLF in bottom right corner of editor, click it and change it to "LF". If you dont do that, you will get errors in my setup.

**Linting Setup**  
In order to lint and format your code automatically according to popular airbnb style guide


**Install Dev Dependencies**  
> yarn add -D eslint prettier  
> npx install-peerdeps --dev eslint-config-airbnb-base  
> yarn add -D eslint-config-prettier eslint-plugin-prettier  


**Setup Linting Configuration file**  
Create a .eslintrc.json file in the project root and enter the below contents:

{  
  "extends": ["prettier", "airbnb-base"],  
  "parserOptions": {  
    "ecmaVersion": 12  
  },  
  "env": {  
    "commonjs": true,  
    "node": true  
  },  
  "rules": {  
    "no-console": 0,  
    "indent": 0,  
    "linebreak-style": 0,  
    "prettier/prettier": [  
      "error",  
      {  
        "trailingComma": "es5",  
        "singleQuote": true,  
        "printWidth": 100,  
        "tabWidth": 4,  
        "semi": true  
      }  
    ]  
  },  
  "plugins": ["prettier"]  
}  


//// Reference- Learn with Sumit - https://github.com/learnwithsumit/nodejs-basic-bangla#install-dev-dependencies 
