sigle env
-------------------------------------
Install env
    npm i dotenv

Create file .env

In file .env
Variable name must begin with "REACT_APP"
//example
    REACT_APP_NANE_SERVER = "LOCAL"

How to use 
//example in file "app.js" you can call 
     {process.env.REACT_APP_NANE_SERVER}

----------------------------------------------
multi env
----------------------------------------------
Install env-cmd
    npm i env-cmd

Create file .env.prod ( You can name it anything example : .env.test .env.develop )
In file .env.prod
//example
    REACT_APP_NANE_SERVER = "PROD"

Write a scripts in "package.json"
//example
    before
        "start": "react-scripts start",
    after
        "start": "env-cmd -f .env react-scripts start",
        "start:prod": "env-cmd -f .env.prod react-scripts start",
        
-----------------------------------------------------------------
when run 
    .env = npm run start
    .env.prod = npm run :prod