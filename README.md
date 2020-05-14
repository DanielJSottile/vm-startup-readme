# Setting Up Your Ubuntu Virtual Machine (Windows and Mac)

You are feel to watch my older brother Anthony's video on setting up this VM!  Most of the screenshots are from this video:

https://youtu.be/qL3xc8hwU7c

Shameless plug, also feel free to check him out if you're interested in Python at all.

# Why a Ubuntu VM?

There's several good reasons for this.

1) It's a Unix style machine, which means STANDARDIZATION!  Most devtools are built to run on Linux, Ubuntu, and other unix style machines, and particularly Windows OS gets left in the dust.  You may have already have found issues arrising with Node and Windows.
2) You don't need to buy another machine. Everything is hosted on your regular machine!
3) Is easily accessible between open windows on your main OS and the VM, meaning you don't have to worry about Dual-Boot systems.
4) Keep your code seperate from everything else on your machine.  A VM gives you a dedicated place where its 100% code material, and you can continue using your OS for leisure, testing, and for whatever you want.

# VirtualBox

## Getting Started

Go to www.virtualbox.org

Here, click the large link which will direct you to https://www.virtualbox.org/wiki/Downloads

Click the "Windows Host" to begin the download and setup.

![Virtual Box](https://imgur.com/9NhQ77Q.png "VIRTUAL BOX")

# VM Setup

## Download It!

First we will be installing the newest version of Ubuntu, 20.04 Focal Fossil.  https://releases.ubuntu.com/20.04/

Choose the Desktop Image

![Focal](https://imgur.com/gTOGdBb.png "Focal")


## In VirtualBox

First, go into Virtual Box and select "New"

![Select New](https://imgur.com/DYFnn9A.png "Select New")


### New Machine

Name your machine Ubuntu20.04
This will help it recognize that it is indeed a Linux Machine.
Make sure the other fields are filled out like this:

![Machine Forms](https://imgur.com/A4FNXPG.png "new machine forms")

## Allocate Memory and Create Hard Disk

### Memory Allocation

Next, you'll allocate the memory in bytes.  Get out your calculators!

This will depend on the RAM on your machine:
8GB Ram -> allocate 3GB (3072 MB)
16GB+ Ram -> allocate 5GB (5120 MB)

In this example, we have a 64GB RAM machine and have allocated 8GB or 8192 MB to it, but honestly you don't need to go above 5GB unless you have that kind of capacity.

![Allocate Memory](https://imgur.com/0siEzLp.png "allocate memory")

### Create a Virtual Hard Disk

Select the Create a Virtual Hard Disk and Continue

![create vhd](https://imgur.com/e3dpLyC.png "create vhd")

### Hard Disk File Type

Don't change anything here and Continue

![Hdd File type](https://imgur.com/iQR8ZXr.png "hdd file type")

### Storage on Hard Disk

Make sure Dynamically Allocated is selected

![dynamically allocated](https://imgur.com/CTmfYFv.png "dynamically allocated")

### File Location and Size

Use the default File Location it chooses.

10GB of hard disk space should be adequate for your VM, though you can go more if you have the space.

![10gb space](https://imgur.com/zseYAMY.png "10 gb space")

PRESS CREATE!  This might take a while, but SSD's go faster.

## Changing Settings

Right Click on your new VM and go into Settings.  You'll only need to change the tabs listed below.

![settings](https://imgur.com/RcUTzZN.png "settings")

### General Settings - Advanced

Go into General Settings

On the Advanced Tab, set Shared Clipboard to Bidirectional.  You can optionally set Drag and Drop to this as well.

![gen settings](https://imgur.com/SRt7Adr.png "gen settings")

### System - Processor

In the System settings on the processor tab...

You can see how many CPU's your machine can handle.  *Set this this to (1/2 - 1) (so if 4, set to 1, 8  set to 3, and 12  set to 5)*

![processor settings](https://imgur.com/igC3bgD.png "processor settings")

Check all the extended features you can.  Some may not be checkable, this is fine.

![processor settings2](https://imgur.com/B0sL75J.png "processor settings2")

### Display - Screen

In the Display settings on the Screen Tab...

Set your Video Memory to MAXIUMUM.

Enable the 3D acceleration.

![vid mem](https://imgur.com/Y9vKSk7.png "vid mem")

### Shared Folders

You'll want to go to this tab and create a Shared Folder.  

When setting the Folder Path, you can name it whatever you like and put it wherever you like, but the convention that's best is to place it next to your VM Folder in ~/VirtualBoxVMs/ and name it Ubuntu20.04_shared.  You'll have to make the folder there before you can select it.

Check the Auto Mount box.

![shared folders](https://imgur.com/lGPI9E4.png "shared folders")

# Ubuntu Setup

Great!  We can now boot our VM by selecting it and pressing the Green Start arrow or double clicking on our VM!

![start](https://imgur.com/S69I1aP.png "start")

## Select Start Up Disk

Now it will prompt you to select the startup disk.  Remember the Disk Image we downloaded earlier?

![select disk](https://imgur.com/1LyTOHL.png "select disk")

Select the disk image either from your downloads folder or wherever you have stored it.  It's probably a good idea to make a directory somewhere on your computer where you can keep these disk images in case you need them later.

![disk](https://imgur.com/cztaKBA.png "disk")

Click start!

Let it do it's thing until it reaches the Installer!

## Installer

You'll see this window.  Of course, we want to install this!

![install](https://imgur.com/f7CTYEC.png "install")

If you have a special keyboard setup, you'll change it in the next window.  Otherwise continue.

## Choosing our Install Settings

Make sure to choose MINIMAL INSTALLATION as otherwise, Ubuntu will install a lot of crap we probably do not need.

Make sure the Download Updates box is checked.

![install settings](https://imgur.com/BrWacqr.png "install settings")

Press Continue

## Installation Type

Make sure that you have Erase Disk and install Ubuntu selected.

Press Install Now

![erase disk](https://imgur.com/w7u0eOJ.png "erase disk")

* DO NOT BE ALARMED ON THE NEXT POP UP * 

Just ignore it and continue!

Next, you'll select your timezone, press continue.

## Who Are You?

Next, you'll be able to set your username and password.  If you are concerned about being able to connect to your SSH on Github (if you have that set up) then you'll want your username to match.  In general, a good convention is all lowercase first character of your first name then last name.  The machine name will autofill and this is fine.

![who are you](https://imgur.com/UHIGqL3.png "who are you")

A password IS recommended for this.  You'll probably need to use it when doing global installations below.  Make sure that the radio button for having it required on login is checked.

![machinename](https://imgur.com/bitCvjk.png "machinename")

Press continue, and the installation will start!

This may take a while, so be patient!

Once it is complete, it will ask you to restart! 

# Once you have set up your Ubuntu VM

Now you can log in and begin setting up your Ubuntu so you can begin coding right away!

## Connect Online Accounts, Other Things

- It will give you a screen to connect online accounts.  I'd connect Google if you have google accounts, but you can skip this.

![onlineacc](https://imgur.com/RNrsiJc.png "onlineacc")

- You can skip setting up Live Patch if you want...or you can set it up.

- You can choose to send or not send info.  Probably best not to send data since you might be working on things.

- Location Services don't matter since you're on a Virtual Machine.

## Opening A Terminal

Ctrl + Alt + T opens a terminal and Ctr + Shift + T opens a new tab in that terminal.  You can also add the Terminal to your favorites list on the side!

## Build Guest Additions Set Up * IMPORTANT * 

Seems like you don't need to do this, but you do!  

In order to work with the Guest Additions, you'll need to go into your terminal and install 3 packages:

`sudo apt update && sudo apt install gcc perl make --no-install-recommends`

![sudo install](https://imgur.com/4mqRJsP.png "sudo install")

Let it do its thing....

## Build Guest Additions

Now you'll go to the upper taskbar and select 'Devices' > 'Insert Guest Additions CD Image'

![insert guest additions](https://imgur.com/YGIjuHe.png "insert guest additions")

This will mount a special 'cd' into your VM and you can run this as an installation!

![run guest additions]https://imgur.com/hQI2Vkl.png "run guest additions")

It will ask for your password, open a new terminal, and install modules.  Once this is done, you'll need to reboot your machine again.

Congratulations, you've officially set up your first (or maybe not your first) Virtual Machine!

----------------------

# Getting Your Machine Up-to-date with Node and JS

## Programs to download

    - Google Chrome (though the pre-installed Firefox works as well, or whatever standard multi-platform browser you use)
    - VS Code 
    - Postman*
    - DBeaver*

That's it.  You'll want to install the .deb versions for Chrome and VS Code, you can do a quick google search to install these again.

For Postman you'll need to type this command in the command prompt to install Postman:
`sudo snap install postman`

For Dbeaver, you'll need to do something similar:
`sudo snap install dbeaver-ce`

Then these will be in your applications and you can drag them onto the side bar as your favorites for quick access!  I'd suggest doing the same for Terminal if you haven't already!

## Setting up VS Code (skip if not using VS Code)

Once you have installed it, similar to Windows, the command for `code` is already set up!

Let's make sure we have a few useful extensions installed.

Go to the extensions toolbar and search for these:

- Beautify
- Bracket Pair Colorizer 2**
- C/C++
- C#
- Debugger for Chrome**
- Debugger for Firefox**
- Docker
- ES7 React/Redux/GraphQL/....
- ESLint**
- HTML CSS Support**
- HTML Snippets
- Language Support for Java
- Live Server**
- PowerShell
- Python
- React Native Tools**
- Ruby
- VSCode Ruby
- vscode-icons**
- WakaTime**
- XML Tools**

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

## Setting up PSQL 

The instructions for doing this are very different from Windows and Mac, so here are the instructions for setting this up.  You can follow the instructions here https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-20-04 but I'll lay them out here as well:

First, go to a terminal and make sure your system's local package index is updated:

`sudo apt update`

Next, put this in your terminal:

`sudo apt install postgresql postgresql-contrib`

Next, you'll want to set up the main role for your postgres server.  That's with this command:

`sudo -u postgres psql postgres`  

We can setup postgres's password if we wish with `\password` once inside our db, but we don't have to.

Next, let's create a superuser with the same name as your Linux User!

`sudo -u postgres createuser --superuser $USER`
`sudo -u postgres psql`

Inside our server, we'll want to set up a password for this user:

`\password [username]`

Now we can quit out of the server and create a db with the same name as our username that we can use as default (you'll see why in a minute)

`sudo -u postgres createdb $USER`

Now quit out of this.  Type `psql` and it'll log into THIS database!

If you want to continue using the postgres database, you can just `psql postgres`

Commands like `createdb test` work on the terminal line.  Everything should be working now!

## Reminder About Git

The first time you use Git in bash it will ask for your username and password for Git.

In VSCode when you do this for the first time, it will ask you for permissions.  Follow it in order to be able to push from the bash inside of VS Code.

# Shoutouts

Once again, this tutorial is based partially off of Anthony Sottile's tutorial on VM set up!  Check out his GH here: https://github.com/asottile 

He does a lot of really cool stuff on his Twitch and YT channels, and hey, he might be the best Python/JavaScript dev I know.  

The rest of this tutorial is based on Thinkful's Engineering Immersion course and what we had to set up to be able to run React, Node, and Postgress.


