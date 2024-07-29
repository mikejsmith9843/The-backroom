# The-backroom
Week-13(Object-Relational-Mapping)

## Table of Contents
1. Description
2. Live Screen-Recording
3. Screenshots
4. Tech Used
5. Installation

## Description
This application was created so that internet retail companies can utilize a MySQL database and keep an up to date record of specific categories, products, and tags related to the sale, and inventory of their e-commerce business. This application uses Sequelize to interact with a MySQL database. The use of an ORM (object-relational-mapping) dependency (Sequelize) rather than strictly using MySQL query's helps make this particular projects code more readable and reusable, and helps further the organization of project code through destructuring of larger files into more manageable pieces. This can also help isolate bugs, keeps the code DRY, and makes code more maintainable for future development.

This project is just the beginning of a complex back end application and can be interacted with through the use of tools such as Insomnia. With Insomnia users can test the functionality of API routes written into the application code which will allow them to view current data, post new data, update data, and delete data from the database (no UI needed).

My main struggles with building the application had to do with the joining of tables. Specifically the relation of Product belongsToMany Tag (through ProductTag) and Tag belongsToMany Product (through ProductTag). Although these relations were fairly simple, I could see how complex they might become, especially if I was strictly set using MySQL query's.

Future development of this application could be taken further through the addition of unit testing, deciding what other areas of a business might need to be added to the database in turn furthering business growth and company organization.

## Live Screen Recording

## Screenshots

## Tech Used
This application is powered by Node.js (v16.19.1), Express.js (v14.17.1), JavaScript, MySQL, and Sequelize (ORM). It utilizes the node package manager (npm) dependencies sequelize (v5.22.5), mysql2 (v2.3.3), express (v4.17.1), dotenv (v8.6.0), and nodemon (v2.0.3). Also, the Insomnia application was utilized to test the functionality of routes within the program.

NodeJS Express.js JavaScript MySQL Sequelize Nodemon Insomnia

## Installation
1. Clone the repo: git clone https://github.com/mikejsmith9843/The-backroom
2. Open VS Code
3. Using the terminal, install node.js v16. If you have homebrew, the command should look like the following (brew install node@16), however this may vary and the documentation should be consulted.
4. Once node.js v16 is installed, in the terminal, utilize the command npm init -y to initialize and create a package.json where project files will be stored.
5. Next, use the terminal to run the command npm i to install the dependencies associated with this application (developers may need to install dependencies directly from the command line).

Commands to install each dependency:

- Command for sequelize will be npm i sequelize
- Command for mysql2 will be npm i mysql2
- Command for express will be npm i express@4.17.1
- Command for dotenv will be npm i dotenv
- Command for nodemon will be npm i nodemon
6. Next, you will need to make sure you have an added .env file within the root directory of your repository, within which you will pass your environmental variables specifying the database name, your MySQL username, and your MySQL password. This will need to be completed before running the application, and will allow the connection.js file to utilize your environmental variables keeping your sensitive information protected.
7. If you do not have a MySQL account, you will need to create one
8. Once all dependencies are installed, you will need to create the database. To do this you will need to navigate to the directory db directory containing the schema.sql file.
9. Once in the MySQL shell you will then run the command source schema.sql. This will create the database.
10. Once the database has been created, you will then need to seed the database (this will also create the model structure for the tables within the database). To do this, navigate to the root directory and run the command npm run seed. This needs to be done from the root directory because the .env file lives within the root.
11. Once the database has been seeded, you will then be able to run the command npm start from the root directory to spin up the server.
12. From there, you can utilize applications such as Insomnia to test the functionality of the routes within the program.