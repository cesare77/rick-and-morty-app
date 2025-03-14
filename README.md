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

`npm istall --save-dev html-webpack-plugin` to install the package needed to adds the minified bundle code to the body tags as script when application running nd then add it to _webpack.config_ file.

`npm install --save-dev webpack-dev-server` to install a local development server that is restarted every time an update is made to any of you application files and then it's needed to change scrpt command in _package.json_ so that it uses _webpack-dev-server_ instead of _Webpack_ from `"start": "webpack --mode development"` to `"start": "webpack serve –mode development"`. (http://localhost:8080/)

We adds some folder to project structures e create some new _Top-level_ (Containers) and _Low-Level_ components and then we retrieve data using _Rick and Morty_ REST API. (https://rickandmortyapi.com/documentation/#rest)

We'll use the built-in state management in React to store data and we'll use for that the `useState` hook.
Anything stored in the state can be passed down from the `top-level` components to `low-level` components via `props`

**useState Hook**
With `useState` hook we can set/store and update these data and every time these data change using the update method that is returned by the `useState Hook` and our component will be re-rendered.

We'll use the Rest Api starting from the analysis of this: https://rickandmortyapi.com/api that returns a Json with all the possible endpoints.

**useEffect Hook**
`useEffect` Hook can be used to hndle side effects, either when the appication mounts or when the `state` or a `prop` ges updated.

This Hook takes two parameters, where the first one is a callback and the second one is an array containing all of the variables this Hook depends on – the so-called dependency array. When any of these dependencies change, the callback for this Hook will be called. When there are no values in this array, the Hook will be called constantly. After the data is fetched from the source, the state will be updated with the results.

I'll use `useEffect` Hook to retrieve data from the API and then i'll update the state with retrieved data.

`npm install --save-dev bootstrap` to install `Bootstrap` package that is a style framework to add style to our simple application and add it to project _devDependecies_, then we add it in the entry point of the application _src/index.js_.

`npm install --save-dev css-loader style-loader` install appropriate loaders to enable Webpack to compile css files and then we'll add these packages as a rule to the Webpack configuration.

> [!NOTE]
> The order in which loaders are added is important since css-loader handles the compilation of the CSS file and style-loader adds the compiled CSS files to the React DOM. Webpack reads these settings from right to left, and the CSS needs to be compiled before it's attached to the DOM.

I'll make some changes to application components to style it through bootstrap. 













