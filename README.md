# Luis-sequelize-notes


## _______________________________________________________

<details><summary>C.R.U.D acronymn: </summary>
<p>

- C - Create
- R - Read
- U - Update
- D - Delete

<p>
</details>

## _______________________________________________________

<details><summary>what is a Database?</summary>
<p>

- A Database is a collection of related information

- Computers are great for storing Databases
- Two types of Databases, Relational & Non-Relational
- Relational Databases uses SQL and store data in tables with rows and columns
- Non-Relational data store data using other data structures

</p>
</details>

## _______________________________________________________

<details><summary>What is Database Management Systems (DBMS)?</summary>
<p>

- Management Systems like PostgreSQL, MySQL, etc.

- Makes it easy to create, maintain and secure a Database.

- Allows you to perform C.R.U.D operations and other administrative tasks. 

</p>
</details>

## _______________________________________________________

<details><summary>Commands to Know</summary>
<p>

<details><summary>sudo -u postgres psql</summary>
<p>

    - Goes to the postgres terminal

</p>
</details>


<details><summary>sudo -u postgres createuser --superuser (YOUR_USER_NAME) </summary>
<p>

    - Creates a user for postgres

</p>
</details>

</p>
</details>


## _______________________________________________________
<details><summary>Sequelize commands to know</summary>
<p>

<details><summary>npm install -g sequelize-cli</summary>
<p>

    - Installs the sequelize command line.

    - "-g" installs it on a global level

</p>
</details>


<details><summary>npm init -y</summary>
    <p>

    - "-y" allows you to say yes to all parameters automatically

    - creates a package.json file and can edit the parameters here

</p>
</details>


<details><summary>npm install sequelize pg express rowdy-logger cors router esj</summary>
<p>

    - Install modules that only belongs to this project ("-g" not included)

    - creates a folder called node_modules that places the modules you installed

<details><summary>What are modules?</summary>
<p>

- A module is the file we use to write our code

- The modules we install is usually files with a group of functions (JavaScript, Python)

- To import a module
    - require('modulePath')

</p>
</details>

</p>
</details>


## _______________________________________________________

<details><summary>How to use migrations to change columns/tables?</summary>
<p>

<details><summary>create a migration file by typing</summary>
<p>

    sequelize migration:generate --name=columnName
</p>
</details>


<details><summary>in the migrations file type above line 11</summary>
<p>

<details><summary>how to rename column?</summary>
<p>

    await queryInterface.renameColumn("psql table", 'oldName', 'newName')
</p>
</details>

<details><summary>how to add columns?</summary>
<p>

    await queryInterface.addColumn("psql table", 'Name', 'dataType')
</p>
</details>


<details><summary>how to remove column?</summary>
<p>

    await queryInterface.removeColumn("psql table", 'columnName')
</p>
</details>

</p>
</details>


<details><summary>after, migrate the file to database</summary>
<p>

    sequelize db:migrate
</p>
</details>





</p>
</details>




</p>
</details>


## _______________________________________________________


<details><summary>How to use migrations to change columns/tables?</summary>
<p>

- create a migration file by typing:
    - <p>sequelize migration:generate --name=columnName</p>


- in the migrations file type above line 11:
    <details><summary>how to rename column?</summary>
    <p>

        await queryInterface.renameColumn("psql table", 'oldName', 'newName')
    </p>
    </details>

    <details><summary>how to add columns?</summary>
    <p>

        await queryInterface.addColumn("psql table", 'Name', 'dataType')
    </p>
    </details>

    <details><summary>how to remove column?</summary>
    <p>

        await queryInterface.removeColumn("psql table", 'columnName')
    </p>
    </details>
<p></p>

- after, migrate the file to database: 
    - sequelize db:migrate


</p>
</details>



## _______________________________________________________

<details><summary>How to seed your database?</summary>
<p>

<details><summary>Create a seed file by typing</summary>
<p>

    sequelize-cli seed:generate --name modelName_seed
</p>
</details>



<details><summary>Populate your table by adding this above line 14</summary>
<p>

- <pre>
    <code>
    await queryInterface.bulkInsert(psql tableName, [
            {
                tableColumn1: columnValue,
                tableColumn2: columnValue,
                createdAt: new Date(),
                updatedAt: new Date()
            },
            {
                tableColumn1: columnValue,
                tableColumn2: columnValue,
                createdAt: new Date(),
                updatedAt: new Date()
            },
    ])
    </code>
  </pre>


</p>
</details>



<details><summary>Seed file into your database</summary>
<p>

    sequelize db:seed:all

</p>
</details>



</p>
</details>


## _______________________________________________________

<details><summary>Sequelize Cheat Sheet</summary>
<p>

- `npm init -y`
- `npm i express pg sequelize rowdy-logger cors`
- add a `.gitignore` and add node_modules and or config to it
- in your package.json add these to the scripts after "test"
- <pre>
  <code>
      "start": "node server.js",
      "dev": "nodemon server.js"
  </code>
  </pre>
- it should look like this
  - <pre>
      <code>
      "scripts": {
      "test": "echo \"Error: no test specified\" && exit 1",
      "start": "node server.js",
      "dev": "nodemon server.js"
    },
      </code>
      </pre>
- `sequelize init`
<details><summary>update config.json (change dialect to postgres)</summary>
<p>

  <pre>
    <code>
    {
        "development": {
            "username": "postgres",
            "password": "password",
            "database": "dbName",
            "host": "127.0.0.1",
            "dialect": "postgresql"
        }
    }
    </code>
  </pre>

</p>
</details>

- create database
- create our model
- Please type this out to get reps in!!
  - `sequelize model:generate --name=tableName --attributes tableColumn:dataType,tableColumn:dataType`
- check your database!
- `sequelize db:migrate`


</p>
</details>

## _______________________________________________________

<details><summary>What are these modules I'm installing?</summary>
<p>


<details><summary>What are modules?</summary>
<p>

- A module is the file we use to write our code

- The modules we install is usually files with a group of functions (JavaScript, Python)

- To import a module
    - require('modulePath')

</p>
</details>

## __________

<details><summary>sequelize</summary>
<p>

- We use sequelize to create our dataBase and perform C.R.U.D functions
        
- sequelize is imported through the models files then, models is imported through the controllers files 

</p>
</details>

## __________

<details><summary>pg</summary>
<p>



</p>
</details>

## __________

<details><summary>express</summary>
<p>

- Express allows us to use our database in a localhost: system.

- this is imported in the server file and routes files

<details><summary>server</summary>
<p>

- we set the express function to a variable called "app"


-  app.use()
    - <p> lets us use what's inside the parameter for the localhost/api </p>


- app.method(urlQuery, callback function) -- (methods like get,post,put)
    - <p>lets us perform C.R.U.D operations depending on the url </p>


- app.listen(portNumber, ()=>{})
    - <p> lets us start the localhost system up </p>



</p>
</details>


<details><summary>routes</summary>
<p>

- gets the router module inside the express file and place it in a variable called "modelRoutes" 

- this will extend the router to this file as well

</p>
</details>




</p>
</details>

## __________


<details><summary>rowdy-logger</summary>
<p>

- rowdy-logger allows us to see what METHOD and URL PATH when we use nodemon

-  This is imported in the sever.js file

<details><summary>Server</summary>
<p>

- import rowdy-logger module as rowdy variable 

- const routesReport = rowdy.begin(app)
    - <p> begin() is a function in the rowdy-logger module that takes the express function as a parameter </p>

- routesReport.print()
    - <p>logs the method and url in terminal </p>

</p>
</details>

</p>
</details>

## __________

<details><summary>cors</summary>
<p>

- makes the front talkable through a .fetch(localhost URL)

- this is imported in the server.js file

<details><summary>server</summary>
<p>

- app.use(cors())
    - <p>this is saying "use the cor function in our localHost/api"</p>

</p>
</details>

</p>
</details>

## __________

<details><summary>router</summary>
<p>

- Router allows us to use our express api in different routes extending from just server.js

- Router is imported in express then used in our routes files

</p>
</details>

## __________

<details><summary>esj</summary>
<p>



</p>
</details>

</p>
</details>
