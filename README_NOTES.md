# TODO: Test this container in bitbucket:
# https://hub.docker.com/r/spittet/node-postgresql/
# https://hub.docker.com/r/nextfaze/node-postgresql-bitbucket-pipelines/
#  
# STEPS TO INCLUE ON Dockerfile to INSTALL PG:
# CREATE FILE :/etc/apt/sources.list.d/pgdg.list
# ADD THIS LINE:
# deb http://apt.postgresql.org/pub/repos/apt/ trusty-pgdg main
apt-get update
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -
apt-get install -y postgresql-9.3 postgresql-client-9.3 postgresql-contrib-9.3
# Verify the version of posgres available:
apt-get update && apt-cache search ^postgresql-9
# Working ok the container in heroku 
# Fowllow the steps:
heroku login
heroku container:login
heroku apps
# >>>gettin' the herokuappname- In this case is:radiant-journey-22301
heroku container:push --app radiant-journey-22301
# NOTE: RUN LOCALLY:
run.sh




# node-js-getting-started

A barebones Node.js app using [Express 4](http://expressjs.com/).

This application supports the [Getting Started with Node on Heroku](https://devcenter.heroku.com/articles/getting-started-with-nodejs) article - check it out.

## Running Locally

Make sure you have [Node.js](http://nodejs.org/) and the [Heroku Toolbelt](https://toolbelt.heroku.com/) installed.

```sh
$ git clone git@github.com:heroku/node-js-getting-started.git # or clone your own fork
$ cd node-js-getting-started
$ npm install
$ npm start
```

Your app should now be running on [localhost:5000](http://localhost:5000/).

## Deploying to Heroku

```
$ heroku create
$ git push heroku master
$ heroku open
```
or

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Documentation

For more information about using Node.js on Heroku, see these Dev Center articles:

- [Getting Started with Node.js on Heroku](https://devcenter.heroku.com/articles/getting-started-with-nodejs)
- [Heroku Node.js Support](https://devcenter.heroku.com/articles/nodejs-support)
- [Node.js on Heroku](https://devcenter.heroku.com/categories/nodejs)
- [Best Practices for Node.js Development](https://devcenter.heroku.com/articles/node-best-practices)
- [Using WebSockets on Heroku with Node.js](https://devcenter.heroku.com/articles/node-websockets)
