# Wallaby.js Automatic Configuration Issue


This repository contains a "new" Nx workspace with one Angular application using Karma and one e2e application (which you get when generating the application) using Cypress. 

Please test the automatic configuration - wihch no longer is working for us since we migrated our workspace from 11.0.20 to @nrwl/workspace > 11.1.4 (where jest is used for automatic configuration?).

### Diagnostic
[Output of Diagnostic can be seen here](https://github.com/whernebrink/wallaby-config-issue/blob/main/DIAGNOSTIC.md)

### Issue
- Unable to do automatic configuration (project nor custom directory). 
- Getting error when having jest deps in package.json (present in node_modules)
- Getting errors not having jest deps in package.json (not present in node_modules)

Without jest-deps in workspace
![Screenshot from VSCode](https://github.com/whernebrink/wallaby-config-issue/blob/main/screenshots/without-jest-deps.png?raw=true)

With jest-deps, Wallaby.js Console
![Screenshot from VSCode](https://github.com/whernebrink/wallaby-config-issue/blob/main/screenshots/with-jest-deps.png?raw=true)

With jest-deps, Wallaby.js Tests (failing test on missing semicolon ect).
![Screenshot from VSCode](https://github.com/whernebrink/wallaby-config-issue/blob/main/screenshots/with-jest-deps-test-fails.png?raw=true)
