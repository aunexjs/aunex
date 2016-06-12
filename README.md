## AuNEX.JS

AuNEX.JS is a project that takes the foundation created by [MEAN.JS](http://meanjs.org) and explores the 
feasibility of several new major concepts that have occurred in the web development world since the dawn of the MEAN
 stack.

AuNEX is a full-stack JavaScript open-source solution, which provides a solid starting point for 
[Aurelia](http://aurelia.io/), [Express](http://expressjs.com/), [Node.js](http://www.nodejs.org/) and Polyglot 
Persistence based applications. The idea is to solve the common issues with connecting those frameworks, build a 
robust framework to support daily development needs, and help developers use better practices while working with 
popular JavaScript components.

## Motivation
MEAN.JS created an excellent starting point for modern SPA's. Most of the principles laid down by the project are still 
 valid however, several trends are developing that diverge from the intent of MEAN.JS enough to warrant an independent 
 project. 

### Aurelia
The biggest breaking change is the use of Aurelia as a front end Framework. Trying to pick a winner of the front end
 framework battles is a fools errand however the principles stated by the Aurelia team seem to be the most solid 
 expression of a stable future I've seen. Therefore the first major goal of AuNEX is to replace Angular 1.0 with 
Aurelia.  

### Polyglot Persistence
The other major change I want to pursue is 
[Polyglot Persistence](http://martinfowler.com/bliki/PolyglotPersistence.html). When the MEAN stack was first proposed, 
MongoDB was becoming a fairly standardized NoSQL solution for startup SPA's. The experience of several large sites 
has shown that scalability is best achieved by storing data in a backend that best matches the structure of the data.
 This is where the 'X' in AuNEX comes in. Projects have a need to utilize many data persistence backends and the
 application has to keep them integrated. Therefore the second major goal of the project is to demonstrate integration
  of multiple data persitence solutions including [MongoDB](https://www.mongodb.com/), [neo4j](http://neo4j.com/), 
   [Cassandra](http://cassandra.apache.org/), RDMS, [Redis](http://redis.io/) and the list goes on.

## Other Concepts
There are a number of other concepts that AuNEX will set out to explore.

### API first
[API First Development](http://apievangelist.com/2014/08/11/what-is-an-api-first-strategy-adding-some-dimensions-to-this-new-question/) places emphasis on developing a strong contract between the backend and front-end as the first 
step to developing a site. A few frameworks have sprung up to support this including [Swagger](http://swagger.io/), 
[api blueprint](https://apiblueprint.org/), [Mashape](https://www.mashape.com//), [Apiary](https://apiary.io/) etc. 
An API first strategy will be taken for AuNEX

### Code Documentation
AuNEX will implement auto-generated code documentation with [jsdoc](http://usejsdoc.org/)

### App Management
Every site needs a solid management foundation. This should include things like:  
1. User Management  
2. Content Management  
3. Site Analytics  
4. Project Management  
5. Server Management  
6. API Management  
7. Documentation  
8. Log Management  
9. Settings Management  
10. Style Guidelines  
11. etc.  

AuNEX will implement a framework to support this.

### Standard Components
The intent of MEAN.JS was to show integration of frameworks. It included a few standard site components such as user 
sign-up, articles etc as examples. These items are repetitive, time consuming and fairly structurally similar 
between sites. The project will attempt to extract these as separately loadable plugins. 

## Before You Begin
Before you begin we recommend you read about the basic building blocks that assemble an AuNEX.JS application:
* Aurelia - A good first step is to go through the [Aurelia documentation](http://aurelia.io/docs.html) and attempt 
to build their example projects. 
* Node.js - Start by going through [Node.js Official Website](http://nodejs.org/) and this [StackOverflow Thread](http://stackoverflow.com/questions/2353818/how-do-i-get-started-with-node-js), which should get you going with the Node.js platform in no time.
* Express - The best way to understand express is through its [Official Website](http://expressjs.com/), which has a [Getting Started](http://expressjs.com/starter/installing.html) guide, as well as an [ExpressJS](http://expressjs.com/en/guide/routing.html) guide for general express topics. You can also go through this [StackOverflow Thread](http://stackoverflow.com/questions/8144214/learning-express-for-node-js) for more resources.
* Persistence - As a minimum you should understand modern NoSQL databases. AuNEX will implement MongoDB so this is a 
good place to get started with the concept of NoSQL however you should expand your knowledge of the various 
alternatives available.

## Prerequisites
Make sure you have installed all of the following prerequisites on your development machine:
* Git - [Download & Install Git](https://git-scm.com/downloads). OSX and Linux machines typically have this already installed.
* Node.js - [Download & Install Node.js](https://nodejs.org/en/download/) and the npm package manager. If you encounter any problems, you can also use this [GitHub Gist](https://gist.github.com/isaacs/579814) to install Node.js.
  * Node v5 IS NOT SUPPORTED AT THIS TIME! 
* MongoDB - [Download & Install MongoDB](http://www.mongodb.org/downloads), and make sure it's running on the default port (27017).
* Ruby - [Download & Install Ruby](https://www.ruby-lang.org/en/documentation/installation/)
* WebPack - You're going to use the [Webpack Module Bundler](http://webpack.github.io/docs/) to manage your front-end
 packages and your build process. Make sure you've installed Node.js and npm first, then install webpack globally using 
 npm:

```bash
$ npm install -g webpack
```
* Sass - You're going to use [Sass](http://sass-lang.com/) to compile CSS during your grunt task. Make sure you have ruby installed, and then install Sass using gem install:

```bash
$ gem install sass
```

## Downloading AuNEX.JS
There are several ways you can get the AuNEX.JS boilerplate:

### Cloning The GitHub Repository
The recommended way to get AuNEX.js is to use git to directly clone the AuNEX.JS repository:

```bash
$ git clone https://github.com/aunexjs/aunex.git aunexjs
```

This will clone the latest version of the AuNEX.JS repository to a **aunexjs** folder.

### Downloading The Repository Zip File
Another way to use the AuNEX.JS boilerplate is to download a zip copy from the [master branch on GitHub](https://github
.com/aunexjs/aunex/archive/master.zip). You can also do this using the `wget` command:

```bash
$ wget https://github.com/aunexjs/aunex/archive/master.zip -O aunexjs.zip; unzip aunexjs.zip; rm aunexjs.zip
```

Don't forget to rename **aunex-master** after your project name.

## Quick Install
Once you've downloaded the boilerplate and installed all the prerequisites, you're just a few steps away from 
starting to develop your AuNEX application.

The first thing you should do is install the Node.js dependencies. The boilerplate comes pre-bundled with a package.json file that contains the list of modules you need to start your application. To learn more about the modules installed visit the npm & Package.json section.

To install Node.js dependencies you're going to use npm again. In the application folder run this in the command-line:

```bash
$ npm install
```

This command does a few things:
* First it will install the dependencies needed for the application to run.
* If you're running in a development environment, it will then also install development dependencies needed for testing and running your application.
* Finally, when the install process is over, npm will initiate a bower install command to install all the front-end modules needed for the application

## Running Your Application
After the install process is over, you'll be able to run your application using Grunt, just run grunt default task:

```
$ webpack watch
```

Your application should run on port 3000 with the *development* environment configuration, so in your browser just go to [http://localhost:3000](http://localhost:3000)

That's it! Your application should be running. To proceed with your development, check the other sections in this documentation.
If you encounter any problems, try the Troubleshooting section.

* explore `config/env/development.js` for development environment configuration options

### Running in Production mode
To run your application with *production* environment configuration, execute grunt as follows:

```bash
$ webpack production
```

* explore `config/env/production.js` for production environment configuration options

### Running with User Seed
To have default account(s) seeded at runtime:

In Development:
```bash
MONGO_SEED=true grunt
```
It will try to seed the users 'user' and 'admin'. If one of the user already exists, it will display an error message on the console. Just grab the passwords from the console.

In Production:
```bash
MONGO_SEED=true grunt prod
```
This will seed the admin user one time if the user does not already exist. You have to copy the password from the console and save it.

### Running with TLS (SSL)
Application will start by default with secure configuration (SSL mode) turned on and listen on port 8443.
To run your application in a secure manner you'll need to use OpenSSL and generate a set of self-signed certificates. Unix-based users can use the following command:

```bash
$ sh ./scripts/generate-ssl-certs.sh
```

Windows users can follow instructions found [here](http://www.websense.com/support/article/kbarticle/How-to-use-OpenSSL-and-Microsoft-Certification-Authority).
After you've generated the key and certificate, place them in the *config/sslcerts* folder.

Finally, execute grunt's prod task `grunt prod`
* enable/disable SSL mode in production environment change the `secure` option in `config/env/production.js`


## Testing Your Application
You can run the full test suite included with MEAN.JS with the test task:

```bash
$ webpack test
```

This will run both the server-side tests (located in the app/tests/ directory) and the client-side tests (located in the public/modules/*/tests/).

To execute only the server tests, run the test:server task:

```bash
$ webpack test:server
```

And to run only the client tests, run the test:client task:

```bash
$ webpack test:client
```

To execute only the tests in a single file:

```bash
$tbd
```

## Running your application with Gulp

After the install process, you can easily run your project with:

```bash
$ gulp
```
or

```bash
$ gulp default
```

The server is now running on http://localhost:3000 if you are using the default settings. 

### Running Gulp Development Environment

Start the development environment with:

```bash
$ gulp dev
```

### Running in Production mode
To run your application with *production* environment configuration, execute gulp as follows:

```bash
$ gulp prod
```

### Testing Your Application with Gulp
Using the full test suite included with MEAN.JS with the test task:

### Run all tests
```bash
$ gulp test
```

### Run server tests
```bash
gulp test:server
```

### Run client tests
```bash
gulp test:client
```

### Run e2e tests
```bash
gulp test:e2e
```

## Development and deployment With Docker

* Install [Docker](https://docs.docker.com/installation/#installation)
* Install [Compose](https://docs.docker.com/compose/install/)

* Local development and testing with compose:
```bash
$ docker-compose up
```

* Local development and testing with just Docker:
```bash
$ docker build -t mean .
$ docker run -p 27017:27017 -d --name db mongo
$ docker run -p 3000:3000 --link db:db_1 mean
$
```

* To enable live reload, forward port 35729 and mount /app and /public as volumes:
```bash
$ docker run -p 3000:3000 -p 35729:35729 -v /Users/mdl/workspace/mean-stack/mean/public:/home/mean/public -v /Users/mdl/workspace/mean-stack/mean/app:/home/mean/app --link db:db_1 mean
```

## Contributing
We welcome pull requests from the community! Just be sure to read the [contributing](https://github.com/aunexjs/aunex/blob/master/CONTRIBUTING.md) doc to get started.

## Deploying To Cloud Foundry

Cloud Foundry is an open source platform-as-a-service (PaaS).  The AuNEXJS project
can easily be deployed to any Cloud Foundry instance.  The easiest way to deploy the
AuNEXJS project to Cloud Foundry is to use a public hosted instance.  The two most popular
instances are [Pivotal Web Services](https://run.pivotal.io/) and
[IBM Bluemix](https://bluemix.net).  Both provide free trials and support pay-as-you-go models
for hosting applications in the cloud.  After you have an account follow the below steps to deploy AuNEXJS.

* Install the [Cloud Foundry command line tools](http://docs.cloudfoundry.org/devguide/installcf/install-go-cli.html).
* Now you need to log into Cloud Foundry from the Cloud Foundry command line.
  *  If you are using Pivotal Web Services run `$ cf login -a api.run.pivotal.io`.
  *  If you are using IBM Bluemix run `$ cf login -a api.ng.bluemix.net`.
* Create a Mongo DB service.
+  *  If you are using Pivotal Web Services run `$ cf create-service mongolab sandbox mean-mongo`
+  *  If you are using IBM Bluemix run `$ cf create-service mongodb 100 mean-mongo`
* Clone the GitHub repo for MEANJS if you have not already done so
  * `$ git clone https://github.com/meanjs/mean.git && cd mean`
* Run `$ npm install`
* Run the Grunt Build task to build the optimized JavaScript and CSS files
  * `$ grunt build`
* Deploy MEANJS to Cloud Foundry
  * `$ cf push`

After `cf push` completes you will see the URL to your running MEANJS application 
(your URL will be different).

    requested state: started
    instances: 1/1
    usage: 128M x 1 instances
    urls: mean-humbler-frappa.mybluemix.net

Open your browser and go to that URL and your should see your MEANJS app running!

###  Deploying AuNEXJS To IBM Bluemix
IBM Bluemix is a Cloud Foundry based PaaS.  By clicking the button below you can signup for Bluemix and deploy
a working copy of AuNEXJS to the cloud without having to do the steps above.

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=https%3A%2F%2Fgithub.com%2Fmeanjs%2Fmean)

After the deployment is finished you will be left with a copy of the AuNEXJS code in your own private Git repo
in Bluemix complete with a pre-configured build and deploy pipeline.  Just clone the Git repo, make your changes, and
commit them back.  Once your changes are committed, the build and deploy pipeline will run automatically deploying
your changes to Bluemix.

## Credits
Inspired by the great work of the [MEAN.JS team](https://github.com/meanjs/)

## License
(The MIT License)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
