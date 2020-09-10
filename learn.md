[] Initialize
    [] mkdir "project name"
    [] cd "project name"
    [] mkdir server cd server
    [] npm init -y
    [] npm i express morgan cors body-parser
    [] touch index.js

server folder
-------------

[] basic initialization of index.js express app (server folder)
    [] bring in express dependency
    [] bring in coors
    [] bring in body-parser
    [] bring in morgan

    ***
    const express = require('express');
    const cors = require('cors');
    const bodyParser = require('body-parser');
    const morgan = require('morgan');
    ***

    [] express app, cors app, morgan app, body-parser app
    
    ***
    const app = express();
    app.use(morgan('tiny'));
    app.use(cors());
    app.use(bodyParser.json());
    ***

    [] first get route
    [] req = request
    [] res = response

    ***
    app.get('/', (req,res) => {
        res.json({
            message = "HELLO WORLD";
        });
    });
    ***

    [] start server on a specific port

    *** 
    const port = process.env.PORT || 1234;
    app.listen(port, () =>{
        console.log(`listening on ${port}`);
    });
    ***

[] install postman to test things
[] npm install --save-dev nodemon
[] in package.json make a start script and one for nodemon also (these are scripts for your command line to run)
    [] inside scripts insert
        "start" : "node index.js"
        "dev" : "nodemon index.js"

client folder
-------------

[] go to root directory of project
[] npx @vue/cli create client






