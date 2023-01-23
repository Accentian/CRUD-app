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

- `yarn global add blitz` 
- `npm install -g blitz`

Test to see if the installation is done correctly using the command: `blitz --help`

If this does not work due to Windows Execution Policy, use the following command: `Set-ExecutionPolicy -ExecutionPolicy Bypass`

- You may need to Run as Administrator in Windows PowerShell 
- You can learn more about Execution Policy here: https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.3

Once we’ve ensured Blitz work, we can begin creating a new app.

## Create a New App in Blitz.js

In your terminal, make sure you are located where you wanted to generate your app.  

Run this command: `blitz new <myAppName>`

- Where `<myAppName>` is the name of your app
  
Blitz will prompt you to select options such as project’s language (I chose JavaScript), app template, and dependencies. Choose what is needed. I used only what was marked Recommended. Your new Blitz app is ready! Next steps, run these commands:
  
- `cd <myAppName>`
- `blitz dev`
  
A message should appear stating that the app can be accessed using this URL: http://localhost:3000

There should already be some predefined features and functions. You will need an account to have full access. Create an account inside the app, or login if you already have one.

## Troubleshooting and Errors
  
You may have issues with the login page and a few other pages. To fix this, locate the problematic files (may vary depending on how you structure the folder) and make these fixes: 
  
- For every `<Link>` (not `</Link>`), modify it to `Link legacyBehavior`
- Example: `<Link legacyBehavior href={Routes.ForgotPasswordPage()}>`

You can read more about it on the [CLI Overview](https://blitzjs.com/docs/cli-overview) documentation.

## Implement a CRUD App

We have the basic app down, now we need to include the features. We’ll be running the `blitz generate` command to create and prepare a few models. To create a simple CRUD app, we’ll be using this link as a reference: https://blitzjs.com/docs/cli-generate

Note that the generalized template is as follows: `blitz generate [type] [model]`

Make sure your terminal is within the folder of your app. Run this particular command line:

```
blitz generate all project name:string description:string
```

- Where `[type]` is `all`
- Where `[model]` is `project` that takes in two strings called *name* and *description*

## Modify the JavaScript to include Description

Because the default models generated possess only `name`, we need to manually modify the JavaScript to allow the `description` to be taken into account. Here are the key files that I had modified and the lines of code that I included into those files.

- ..\src\projects\components\ProjectForm.js
> `<LabeledTextField name="description" label="description" placeholder="Description" />`

- ..\src\projects\mutations\updateProject.js
> `description: z.string(),`

- ..\src\projects\mutations\createProject.js
> `description: z.string(),`

## Modifiy Database Provider from SQLite to MySQL

The default provider is SQLite. We can switch over to MySQL and MongoDB. As of now, only MySQL has been successfully switched from SQLite. To begin, we must have MySQL installed into our computer. Your setup may be different and may include MySQL. If you do not have MySQL, you can install MySQL using this link: https://dev.mysql.com/downloads/installer/

To make the switch from SQLite to MySQL, we first need to modify the following files:

- schema.prisma
> `DATABASE_URL="mysql://USER:PASSWORD@HOST:PORT/DATABASE”`

```
Host    HOST	    IP address/domain of your database server, e.g. localhost

Port    PORT	    Port on which your database server is running, e.g. 5432

User    USER	    Name of your database user, e.g. janedoe

Password    PASSWORD	Password for your database user

Database    DATABASE	Name of the database you want to use, e.g. mydb
```

- .env.local
> `provider = “sqlite“ -> provider = "mysql"`

After the modification is made, run this command line: 

`blitz prisma migrate dev`

If there's an issue regarding migration, delete the **`migragtions`** folder located in the **`db`** folder and try again.

## Update and Run the CRUD App

Once the command is executed successfully, the terminal will prompt the user to update the database.  Allow the database to be updated. 

Run `blitz dev` to refresh and open the app and select `‘Go to /projects’`

If there’s any errors regarding `<Link>` and `<a>`, refer to the **Troubleshooting and Errors** section.


You will see a link called **“Create Project”** and two buttons named *Previous* and *Next*.

- Click on Create Project
- You will be redirected to another page. Enter the name of your project and hit the button “Create Project”
- Fill out Name and Description fields and have fun creating, reading, updating, and deleting 


**References Used:**

https://www.prisma.io/docs/concepts/database-connectors/mysql

https://blitzjs.com/docs/database-overview

https://www.youtube.com/watch?v=xqbGZUHwqWE


## Learn more

Read the [Blitz.js Documentation](https://blitzjs.com/docs/getting-started) to learn more.

The Blitz community is warm, safe, diverse, inclusive, and fun! Feel free to reach out to us in any of our communication channels.

- [Website](https://blitzjs.com)
- [Discord](https://blitzjs.com/discord)
- [Report an issue](https://github.com/blitz-js/blitz/issues/new/choose)
- [Forum discussions](https://github.com/blitz-js/blitz/discussions)
- [How to Contribute](https://blitzjs.com/docs/contributing)
- [Sponsor or donate](https://github.com/blitz-js/blitz#sponsors-and-donations)
