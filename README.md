# E-Commerce Site

## Description

This application utilizes a back-end, express server to allow the user to build and operate their own e-commerce site. E-commerce has become a staple for businesses both large and small, allowing sellers to provide products to customers across the globe.

The app functions through the REST API tool Insomnia.

[View the Insomnia Website](https://insomnia.rest/)

[View the video demo](https://drive.google.com/file/d/137JCJ8ZVsHBJnUGLefhVy06ewVp81YGE/view?usp=sharing)

## Setup

To begin, the user opens the command line terminal in the same folder as the server.js file. The command line terminal can be opened by right clicking on the server.js file and clicking on the option "Open in Integrated Terminal."

### Initialization

This section outlines the process of installing the package.json file. If the package.json file already exists, please skip ahead to the [installation](###installation) section.


For the app to operate, the user must install the necessary npm packages (mysql and inquirer). Installation requires a package.json file in the repository's main folder (or the same folder as the server.js file). To install the package.json file, the user inputs the following command into the terminal to initialize Node.js and install the file:

```
npm init -y
```

### Installation

Once the package.json file has been installed, the user may install the npm packages required for the app to function. First, check the "dependencies" section of the package.json file. If both inquirer and mysql are listed as dependencies, the user runs the following command to install the node modules for both packages:

```
npm i
```

If mysql does not appear as a dependency, the user runs the following command to install it:

```
npm i mysql
```

if inquirer does not appear as a dependency, the user runs the following command to install it:

```
npm i inquirer
```

### Connecting to the database

In order to add information to the database, the user must initialize mysql. To do this the user runs the following command:

```
mysql -u root -p
```

The user will be prompted to enter the database password, which is simply "password" (note, password is case sensitive). If done correctly, the user will enter the mysql terminal. From there, the user will input the following command to connect to the mysql database

```
source db/schema.sql
```

This command will run the program in the schema.sql file, which builds the database and creates and seeds the tables. To connect the database to the application, the user inputs the following command:

```
use employee_trackerdb
```

Once the database is connected, the user may exit the mysql terminal by inputting "exit" or "quit"

### Seeding the database

To add the data from the seeds folder, the user inputs the following command:

```
node seeds/seed.js
```

### Usage

To use the app, the user opens the Insomnia application and creates a new route collection by clicking the purple "create" button in the upper right corner of the window. From there, the user may run API functions by inputting the server URL along with the corresponding HTTP method. Insomnia will run the command.

## Contributors

* Leighton Albrecht