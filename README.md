[![Blitz.js](https://raw.githubusercontent.com/blitz-js/art/master/github-cover-photo.png)](https://blitzjs.com)

This is a [Blitz.js](https://github.com/blitz-js/blitz) app.

# ****CRUD App****

Request: Document your learning and teach others while you create a CRUD app using Blitz.js. There should be authentication. Also, have Blitz interface with MySQL and MongoDB. Create a GitHub repo: Where your Readme serves as a Tutorial.

CRUD is an acronym for four functions that are considered necessary to implement a persistent storage application: create, read, update and delete.

## System and Applications used
Project performed on:

-	Windows 11
-	Visual Code Studio
-	Windows PowerShell or Visual Code Studio Terminal
- Node.js
- Blitz.js

## Running the Blitz.js app

Run your app in the development mode. To do this, open a terminal of your choice. Ensure that you're located in the folder/directory that the app is in, then run the following command:

```
blitz dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

# Manually Creating this Blitz.js CRUD App: Installation and Setup

The following is a tutorial on how to develop the exact CRUD app displayed in this repo. You need to install Blitz.js and Node.js. I would recommend starting from here through this link: https://blitzjs.com/docs/get-started#set-up-your-computer. 

Check the version using Windows PowerShell or another terminal using the command `node -v`. 

- If not, download Node.js from their website: https://nodejs.org/en/download/

You can install Blitz using either of these commands: 

- yarn global add blitz 
- npm install -g blitz

Test to see if the installation is done correctly using the command: `blitz --help`

If this does not work due to Windows Execution Policy, use the following command: `Set-ExecutionPolicy -ExecutionPolicy Bypass`

- You may need to Run as Administrator in Windows PowerShell 
- You can learn more about Execution Policy here: https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.3

Once we’ve ensured Blitz work, we can begin creating a new app.

## Create a New App in Blitz.js

In your terminal, make sure you are located where you wanted to generate your app.  

Run this command: `blitz new <myAppName>`
- Where <myAppName> is the name of your app
  
Blitz will prompt you to select options such as project’s language (I chose JavaScript), app template, and dependencies. Choose what is needed. I used only what was marked Recommended. Your new Blitz app is ready! Next steps, run these commands:
  
- `cd <myAppName>`
- `blitz dev`
  
A message should appear stating that the app can be accessed using this URL: http://localhost:3000

There should already be some predefined features and functions. You will need an account to have full access. Create an account, or login if you already have one.

## Commands

Blitz comes with a powerful CLI that is designed to make development easy and fast. You can install it with `npm i -g blitz`

```
  blitz [COMMAND]

  dev       Start a development server
  build     Create a production build
  start     Start a production server
  export    Export your Blitz app as a static application
  prisma    Run prisma commands
  generate  Generate new files for your Blitz project
  console   Run the Blitz console REPL
  install   Install a recipe
  help      Display help for blitz
  test      Run project tests
```

You can read more about it on the [CLI Overview](https://blitzjs.com/docs/cli-overview) documentation.

## Learn more

Read the [Blitz.js Documentation](https://blitzjs.com/docs/getting-started) to learn more.

The Blitz community is warm, safe, diverse, inclusive, and fun! Feel free to reach out to us in any of our communication channels.

- [Website](https://blitzjs.com)
- [Discord](https://blitzjs.com/discord)
- [Report an issue](https://github.com/blitz-js/blitz/issues/new/choose)
- [Forum discussions](https://github.com/blitz-js/blitz/discussions)
- [How to Contribute](https://blitzjs.com/docs/contributing)
- [Sponsor or donate](https://github.com/blitz-js/blitz#sponsors-and-donations)
