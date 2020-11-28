# npm-preinstall-bug
From node 15.0.0 npm install command executes preinstall script AFTER installing dependencies.

to reproduce just clone this repo and run `npm install`

the expected result is `preinstall` script in `package.json` to be executed BEFORE dependencies installation.

the reality is - `preinstall` script will be executed AFTER dependencies installation.

how can you check this - after executing `npm install` you will see that `node_modules` directory was deleted by `preinstall` script.

Note: mongodb is just an example dependency package. You can try with any other npm package as dependency.
