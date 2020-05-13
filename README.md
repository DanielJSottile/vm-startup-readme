# Once you have set up your VM

## Programs to download

    - Google Chrome (though Firefox works as well)
    - VS Code 

That's it.  You'll want to install the .deb versions

## Setting up VS Code (skip if not using VS Code)

Once you have installed it, similar to Windows, the command for `code` is already set up!

Let's make sure we have a few useful extensions installed.

Go to the extensions toolbar and search for these:

- Beautify
- Bracket Pair Colorizer 2
- C/C++
- C#
- Debugger for Chrome
- Debugger for Firefox
- Docker
- ES7 React/Redux/GraphQL/....
- ESLint
- HTML CSS Support
- HTML Snippets
- Language Support for Java
- Live Server
- PowerShell
- Python
- React Native Tools
- Ruby
- VSCode Ruby
- vscode-icons
- WakaTime
- XML Tools

When you install WakaTime, the first time you write code it will ask for your api key from the link.  Put it in.

You'll also need to fix your tabs.  Go to Preferences > Settings, Turn on Tab Completion and go to Editor: Tab Size and change it to 2

## Setting up NODE

While Ubuntu has a built in NPM, it is much better for us to install it directly from the nodesource ppa.  You can find the Binary Distributions here: https://github.com/nodesource/distributions

We are only interested in the Ubuntu Node.js v12.x, so paste these instructions in your terminal:

```
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs
```

This will install Node for you to use.

## Setting up Special Global Packages

Let's set up a few global packages.  Ubuntu differs slightly from other UNIX shells in that we do need to call `sudo` on certain global installations.  Let's make sure we have the latest version of NPM

`sudo npm install -g npm@latest` - latest npm

`sudo npm install -g n` - This is N, which lets us control our version of Node we are on.  Typing `n lts` will show the last stable version of Node, while `n latest` will show the latest version.  By typing `n [version#]` you will install that version of Node.  By typing the command `n` you will be able to scroll and choose which Node you want to use.



## Installing EsLint

As a reminder, we run this command:

`npm install -g eslint`

now `cd ~`, then `touch .eslintrc.json` then `code .eslintrc.json`

Then, paste this in the file: 


```
{
    /** 
    * ESLint: http://eslint.org/docs/user-guide/configuring
    */

    // "env:" supplies predefined global variables
    "env": {
        "browser": true,
        "es6": true,
        "node": true,
        "mocha": true,
        "mongo": true
    },
    // our configuration extends the recommended base configuration
    "extends": "eslint:recommended",
    // define the type of file `script` or `module` for ES6 Modules
    "parserOptions": {
        "sourceType": "module"
    },
    //ESLint rules: Severity Levels: off = 0 | warn = 1 | error = 2
    "rules": {
        "strict": ["error", "safe"],   //prefer `'use-strict';` pragma
        "eqeqeq":"error",              //prefer strict equality `===`
        "no-console": "warn",          //allows but warn about console like `console.log()`
        "no-unused-vars": "warn",      //warns about unused variables
        "no-eval": "error",            //disallows `eval()` usage
        "indent": ["error", 2],        //enforce 2 space indents (not tabs)        
        "quotes": ["error", "single"], //prefer single quotes over double quotes
        "semi": ["error", "always"]    //enforce semi-colon usage
    }
}
```

## Reminder About Git

not sure yet... testing


