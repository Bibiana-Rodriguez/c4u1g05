# c4u1g05
var express = require("express");
//npmvar bodyParser = require("body-parser");
var app = express();

//var chocolate_router = require('./routers/Chocolate');
//var mongoose = require('mongoose');


app.use(express.json());
app.use(express.urlencoded({
extended: true
}));


app.use((req, res, next) => {
    res.header('Access-Control-Allow-Origin', '*');
    res.header('Access-Control-Allow-Headers', 'Authorization, X-API-KEY, Origin, XRequested-With, Content-Type, Accept, Access-Control-Allow-Request-Method');
    res.header('Access-Control-Allow-Methods', 'GET, POST, OPTIONS, PUT, DELETE');
    res.header('Allow', 'GET, POST, OPTIONS, PUT, DELETE');
    next();
    });

    app.use(require('../PROYECTO_NJS/routers/routes.js'))
    module.exports = app;
