# NODE.JS

![node](/img/1200px-Node.js_logo.svg.png)



## What Is Node.js?
There are plenty of definitions to be found online. Let’s take a look at a couple of the more popular ones.

## Node Is Built on Google Chrome’s V8 JavaScript Engine
The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.

However, when we say that Node is built on the V8 engine, we don’t mean that Node programs are executed in a browser. They aren’t. Rather, the creator of Node (Ryan Dahl) took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.

This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

## How Do I Install Node.js?
In this next section, we’ll install Node and write a couple of simple programs. We’ll also look at npm, a package manager that comes bundled with Node.


### Node Binaries vs Version Manager

Many websites will recommend that you head to the official Node download page and grab the Node binaries for your system. While that works, I would suggest that you use a version manager instead. This is a program that allows you to install multiple versions of Node and switch between them at will. There are various advantages to using a version manager. For example, it negates potential permission issues when using Node with npm and lets you set a Node version on a per-project basis.

If you fancy going the version manager route, please consult our quick tip: Install Multiple Versions of Node.js using nvm. Otherwise, grab the correct binaries for your system from the link above and install those.

### “Hello, World!” the Node.js Way
You can check that Node is installed on your system by opening a terminal and typing ``node -v``. If all has gone well, you should see something like ``v12.14.1 displayed``. This is the current LTS version at the time of writing.

Next, create a new file ``hello.js`` and copy in the following code:
```
console.log("Hello, World!");
```


## Introducing npm, the JavaScript Package Manager
As I mentioned earlier, Node comes bundled with a package manager called npm. To check which version you have installed on your system, type ``npm -v``.

In addition to being the package manager for JavaScript, npm is also the world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week. Let’s take a quick look at how we would use npm to install a package.

### Installing a Package Globally
Open your terminal and type the following:
```
npm install -g jshint
```
This will install the jshint package globally on your system. We can use it to lint the ``index.js`` file from the previous example:

```
jshint index.js
```

### Installing a Package Locally
We can also install packages locally to a project, as opposed to globally, on our system. Create a test folder and open a terminal in that ``directory.`` Next type this:
```
npm init -y
```

This will create and auto-populate a ``package.json`` file in the same folder. Next, use npm to install the lodash package and save it as a project dependency:
```
npm install lodash --save
```
Create a file named ``test.js`` and add the following:
```
const _ = require('lodash');

const arr = [0, 1, false, 2, '', 3];
console.log(_.compact(arr));
```
Finally, run the script using node ``test.js.``  You should see ```[ 1, 2, 3 ]``` output to the terminal.

