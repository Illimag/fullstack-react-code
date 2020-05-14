# Code examples for the React Book

## Setup

Please refer to the first chapter in the book for instructions on setting up your environment with Node & npm.

## Installing packages for all projects

You can install all the packages for all the projects up front, saving you time in the future. To do so, from this directory:

```
npm i
npm run install-all
```

Unless you have a quantum computer connected directly to an Amazon data center, this task will take a long time to complete.

## JK

Machine OS: 

    Ubuntu20.04 LTS

For errors during using command:

    sudo npm run install-all

Just install the dependencies manually in the folders in the errors. Installing the dependencies globally in the main project file sometimes works with dependencies such as webpack. But for others as well as being able to audit, the command will have to run in the individual project files.

Later the individual project package.json can be adjusted accordingly to remove all error codes, because some of the dependencies are no longer supported.

To run audit:

    sudo npm audit fix

If errors such as:

ERROR LOG:

    npm ERR! code ELIFECYCLE
    npm ERR! errno 1
    npm ERR! fullstack-react-code@17.0.0 install-all: `npm-recursive-install`
    npm ERR! Exit status 1
    npm ERR! 
    npm ERR! Failed at the fullstack-react-code@17.0.0 install-all script.
    npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

    npm ERR! A complete log of this run can be found in:

Check log to see if there any of these additional errors:

To fix error we can manually enter folder system and install dependencies.

When the fullstack-react-code@17.0.0 script is run, it automatically runs npm install in each folder. If there are any error code related to the local dependencies.

    npm audit fix

Will need to run command in each folder.

Depending on the error message just install the dependency in the folder that has the package.json.

If that doesn't fix the problem then try cleaning the cache, removing the node_modules dir, and doing a fresh install of the package.json with npm.

    sudo npm cache clean

    sudo rm -rf node_modules

    sudo npm install

## For npm errors:

npm WARN extract-text-webpack-plugin@3.0.0 requires a peer of webpack@^3.1.0 but none is installed. You must install peer dependencies yourself.

npm WARN loaders@1.1.3 requires a peer of webpack@1 || 2 but none is installed. You must install peer dependencies yourself.

    sudo npm install webpack@1 || 2

Or 

    sudo npm install webpack@2 || 3

Depending on the following error messages related to webpack, can't have multiple verisons of webpack installed.

So for example installing:

    sudo npm install webpack@^4

In the main folder could be the solution.

npm WARN react-dom@16.13.1 requires a peer of react@^16.13.1 but none is installed. You must install peer dependencies yourself.

    sudo npm install --global webpack webpack-dev-server

npm WARN ajv-keywords@3.4.1 requires a peer of ajv@^6.9.1 but none is installed. You must install peer dependencies yourself.

    sudo npm install ajv

Install fsevents on Ubuntu with force arguement

    sudo npm install -f fsevents

Installing react errors

Just install based on version number.

Install fullstack-react-code

    sudo npm run install-all

## Running the code

See the respective `README.md` for each project.