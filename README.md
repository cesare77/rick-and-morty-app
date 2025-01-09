# rick-and-morty-app

React Application that retrieve via API info about TV show Rick and Morty.

## Git commands mostly used

- `git remote add origin <repository url>` to sync project to remote
- `git push --force -u -origin master` to push to remote
- `git add .` to add changes to commit
- `git commit -m "message"` to do commit with message
- `git push -u origin master` to push changes to origin
- `git log --oneline` to view commit logs
- `git status` to view current git status

## Starting project setup

**Create Package.json**
`npm init -y` to create package.json file inside the empty project folder.
`-y` flag is to skip the steps to set information such as the name, version, etc.

**Setting up and configuring Webpack and Babel**
`npm install --save-dev webpack webpack-cli` to install webpack and webpack-cli as _devDependecies_.
Add to the _scripts_ section of package.json two commands to start and build application with webpack.
After that it's possible to run start command to create main file and run this file to check the current app status.
`node dist/main.js` that execute console command inside file.

`npm install react react-dom` to install packages needed to run a React application.

`npm install --save-dev @babel/core babel-loader @babel/preset-env @babel/preset-react` to install as _devDependencies_
Babel Core, babel-loader helper and two preset package for complation purpose.
Add two file for configuration: _babel.config.json_ and _webpack.config.js_.

> [!NOTE]
> The configuration for _babel-loader_ can also be placed in the configuration inside _webpack.config.json_. But by creating a separate Babel configuration file for this, these settings can also be used by other tools in the JavaScript/React ecosystem.




