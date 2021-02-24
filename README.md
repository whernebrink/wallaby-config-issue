A nex Nx workspace with Angular application using Karma and Cypress as test runners to test automatic configuration for Wallaby.js - Not working.

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
