# LoopBack Workspace 3.0

## About

The `loopback-workspace` module provides node.js and REST APIs for interacting
with a set of loopback components. Components are organized in the following
basic directory structure:

```txt
  /my-workspace
    /my-component-a
    /my-component-b
    /my-component-c
    package.json
```

Each component has the following basic structure:

```txt
  /my-component
    config.json
    datasources.json
    model-config.json
    /models
      my-model.json
      my-model.js
```

## Usage

**Basic**

The `loopback-workspace` itself is a loopback component. The following
will load the workspace in the current working directory (`process.cwd()`).

```js
// workspace is a loopback `app` object
var workspace = require('loopback-workspace');
```

**Custom Workspace Directory**

To start the workspace in a specific directory, specify the `WORKSPACE_DIR` env
variable.

**REST**

In order to use the REST api, mount the app on an existing express app or call
`workspace.listen(PORT)`.

## Test

**To run end-to-end tests, you will need a local MySQL instance.**

Run `node test/helpers/setup-mysql.js` to create a test database and
a test user. This is a one-time task to run only once when setting up your
development environment.

Use the `npm test` command to run the tests.
