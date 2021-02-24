```
{
  editorVersion: '1.53.2',
  pluginVersion: '1.0.268',
  editorType: 'VSCode',
  osVersion: 'darwin 19.6.0',
  nodeVersion: 'v14.13.0',
  coreVersion: '1.0.1034',
  checksum: 'OTg4OGZkOWE5OTRlMzNlYWNlMjFmZmJiMjU1ZWVlZTQsMTY0NDk2OTYwMDAwMCww',
  config: {
    diagnostics: {
      angular: {
        workspace: {
          version: 1,
          cli: { defaultCollection: '@nrwl/angular' },
          defaultProject: 'm3-client',
          schematics: {
            '@nrwl/angular': { application: { linter: 'eslint' }, library: { linter: 'eslint' }, 'storybook-configuration': { linter: 'eslint' } },
            '@nrwl/angular:application': { style: 'scss', linter: 'eslint', unitTestRunner: 'karma', e2eTestRunner: 'cypress', strict: true },
            '@nrwl/angular:library': { style: 'scss', linter: 'eslint', unitTestRunner: 'karma' },
            '@nrwl/angular:component': { style: 'scss' }
          },
          projects: {
            'm3-client': {
              projectType: 'application',
              root: 'apps/m3-client',
              sourceRoot: 'apps/m3-client/src',
              prefix: 'm3',
              architect: {
                build: {
                  builder: '@angular-devkit/build-angular:browser',
                  options: {
                    outputPath: 'dist/apps/m3-client',
                    index: 'apps/m3-client/src/index.html',
                    main: 'apps/m3-client/src/main.ts',
                    polyfills: 'apps/m3-client/src/polyfills.ts',
                    tsConfig: 'apps/m3-client/tsconfig.app.json',
                    aot: true,
                    assets: [ 'apps/m3-client/src/favicon.ico', 'apps/m3-client/src/assets' ],
                    styles: [ 'apps/m3-client/src/styles.scss' ],
                    scripts: []
                  },
                  configurations: {
                    production: {
                      fileReplacements: [ { replace: 'apps/m3-client/src/environments/environment.ts', with: 'apps/m3-client/src/environments/environment.prod.ts' } ],
                      optimization: true,
                      outputHashing: 'all',
                      sourceMap: false,
                      namedChunks: false,
                      extractLicenses: true,
                      vendorChunk: false,
                      buildOptimizer: true,
                      budgets: [ { type: 'initial', maximumWarning: '2mb', maximumError: '5mb' }, { type: 'anyComponentStyle', maximumWarning: '6kb', maximumError: '10kb' } ]
                    }
                  }
                },
                serve: {
                  builder: '@angular-devkit/build-angular:dev-server',
                  options: { browserTarget: 'm3-client:build' },
                  configurations: { production: { browserTarget: 'm3-client:build:production' } }
                },
                'extract-i18n': { builder: '@angular-devkit/build-angular:extract-i18n', options: { browserTarget: 'm3-client:build' } },
                lint: { builder: '@nrwl/linter:eslint', options: { lintFilePatterns: [ 'apps/m3-client/src/**/*.ts', 'apps/m3-client/src/**/*.html' ] } },
                test: {
                  builder: '@angular-devkit/build-angular:karma',
                  options: {
                    main: 'apps/m3-client/src/test.ts',
                    tsConfig: 'apps/m3-client/tsconfig.spec.json',
                    karmaConfig: 'apps/m3-client/karma.conf.js',
                    polyfills: 'apps/m3-client/src/polyfills.ts',
                    styles: [],
                    scripts: [],
                    assets: []
                  }
                }
              }
            },
            'm3-client-e2e': {
              root: 'apps/m3-client-e2e',
              sourceRoot: 'apps/m3-client-e2e/src',
              projectType: 'application',
              architect: {
                e2e: {
                  builder: '@nrwl/cypress:cypress',
                  options: { cypressConfig: 'apps/m3-client-e2e/cypress.json', tsConfig: 'apps/m3-client-e2e/tsconfig.e2e.json', devServerTarget: 'm3-client:serve' },
                  configurations: { production: { devServerTarget: 'm3-client:serve:production' } }
                },
                lint: { builder: '@nrwl/linter:eslint', options: { lintFilePatterns: [ 'apps/m3-client-e2e/**/*.{js,ts}' ] } }
              }
            }
          }
        }
      },
      jest: {
        config: {
          configs: [
            {
              automock: false,
              cache: true,
              cacheDirectory: '/private/var/folders/nt/5y6phytd77958fzy5s4gn390q8qrtt/T/jest_cwxtga',
              clearMocks: false,
              coveragePathIgnorePatterns: [ '/node_modules/' ],
              cwd: '<homeDir>/Developer/remove-me',
              dependencyExtractor: undefined,
              detectLeaks: undefined,
              detectOpenHandles: undefined,
              displayName: undefined,
              errorOnDeprecated: false,
              extraGlobals: [],
              filter: undefined,
              forceCoverageMatch: [],
              globalSetup: undefined,
              globalTeardown: undefined,
              globals: {},
              haste: { computeSha1: false, throwOnModuleCollision: false },
              injectGlobals: true,
              moduleDirectories: [ 'node_modules' ],
              moduleFileExtensions: [ 'js', 'json', 'jsx', 'ts', 'tsx', 'node' ],
              moduleLoader: undefined,
              moduleNameMapper: [],
              modulePathIgnorePatterns: [],
              modulePaths: undefined,
              name: 'dc580a642e2b31611cd843479b0a2122',
              prettierPath: 'prettier',
              resetMocks: false,
              resetModules: false,
              resolver: undefined,
              restoreMocks: false,
              rootDir: '<homeDir>/Developer/remove-me',
              roots: [ '<homeDir>/Developer/remove-me' ],
              runner: 'jest-runner',
              setupFiles: [],
              setupFilesAfterEnv: [],
              skipFilter: false,
              skipNodeResolution: undefined,
              slowTestThreshold: 5,
              snapshotResolver: undefined,
              snapshotSerializers: [],
              testEnvironment: '<homeDir>/Developer/remove-me/node_modules/jest-environment-jsdom/build/index.js',
              testEnvironmentOptions: {},
              testLocationInResults: false,
              testMatch: [ '**/__tests__/**/*.[jt]s?(x)', '**/?(*.)+(spec|test).[tj]s?(x)' ],
              testPathIgnorePatterns: [ '/node_modules/' ],
              testRegex: [],
              testRunner: '<homeDir>/Developer/remove-me/node_modules/jest-jasmine2/build/index.js',
              testURL: 'http://localhost',
              timers: 'real',
              transform: [ [ '\\.[jt]sx?$', '<homeDir>/Developer/remove-me/node_modules/babel-jest/build/index.js', {} ] ],
              transformIgnorePatterns: [ '/node_modules/', '\\.pnp\\.[^\\/]+$' ],
              unmockedModulePathPatterns: undefined,
              watchPathIgnorePatterns: []
            }
          ],
          globalConfig: {
            bail: 0,
            changedFilesWithAncestor: false,
            changedSince: undefined,
            collectCoverage: false,
            collectCoverageFrom: [],
            collectCoverageOnlyFrom: undefined,
            coverageDirectory: '<homeDir>/Developer/remove-me/coverage',
            coverageProvider: 'babel',
            coverageReporters: [ 'json', 'text', 'lcov', 'clover' ],
            coverageThreshold: undefined,
            detectLeaks: undefined,
            detectOpenHandles: undefined,
            enabledTestsMap: undefined,
            errorOnDeprecated: false,
            expand: false,
            filter: undefined,
            findRelatedTests: false,
            forceExit: false,
            globalSetup: undefined,
            globalTeardown: undefined,
            json: false,
            lastCommit: false,
            listTests: undefined,
            logHeapUsage: false,
            maxConcurrency: 5,
            maxWorkers: 11,
            noSCM: undefined,
            noStackTrace: false,
            nonFlagArgs: undefined,
            notify: false,
            notifyMode: 'failure-change',
            onlyChanged: false,
            onlyFailures: false,
            outputFile: undefined,
            passWithNoTests: undefined,
            projects: [],
            replname: undefined,
            reporters: undefined,
            rootDir: '<homeDir>/Developer/remove-me',
            runTestsByPath: false,
            silent: undefined,
            skipFilter: false,
            testFailureExitCode: 1,
            testNamePattern: undefined,
            testPathPattern: '',
            testResultsProcessor: undefined,
            testSequencer: '<homeDir>/Developer/remove-me/node_modules/@jest/test-sequencer/build/index.js',
            testTimeout: undefined,
            updateSnapshot: 'new',
            useStderr: false,
            verbose: undefined,
            watch: false,
            watchAll: false,
            watchPlugins: undefined,
            watchman: true
          },
          hasDeprecationWarnings: false,
          wallaby: {
            roots: [],
            watchPathIgnorePatterns: [ '/node_modules/', '\\./dist/|\\./build/|\\./coverage/|/\\..+/' ],
            testPathIgnorePatterns: [ '/node_modules/', '\\./dist/|\\./build/|\\./coverage/|/\\..+/' ],
            testMatch: [ '**/__tests__/**/*.[jt]s?(x)', '**/?(*.)+(spec|test).[tj]s?(x)' ],
            testRegex: []
          }
        }
      }
    },
    testFramework: { version: 'jest@24.8.0', configurator: 'jest@24.8.0', reporter: 'jest@24.8.0', starter: 'jest@24.8.0', autoDetected: true },
    filesWithCoverageCalculated: [],
    filesWithNoCoverageCalculated: [],
    globalSetup: false,
    micromatch: true,
    files: [
      { pattern: '/node_modules/', regexp: /\/node_modules\//, ignore: true, trigger: true, load: true },
      { pattern: '\\./dist/|\\./build/|\\./coverage/|/\\..+/', regexp: /\.\/dist\/|\.\/build\/|\.\/coverage\/|\/\..+\//, ignore: true, trigger: true, load: true },
      { pattern: '**/**', ignore: false, trigger: true, load: true, order: 1 },
      { pattern: '**/__tests__/**/*.[jt]s?(x)', ignore: true, trigger: true, load: true },
      { pattern: '**/?(*.)+(spec|test).[tj]s?(x)', ignore: true, trigger: true, load: true }
    ],
    tests: [
      { pattern: '/node_modules/', regexp: /\/node_modules\//, ignore: true, trigger: true, load: true, test: true },
      { pattern: '\\./dist/|\\./build/|\\./coverage/|/\\..+/', regexp: /\.\/dist\/|\.\/build\/|\.\/coverage\/|\/\..+\//, ignore: true, trigger: true, load: true, test: true },
      { pattern: '**/__tests__/**/*.[jt]s?(x)', ignore: false, trigger: true, load: true, test: true, order: 2 },
      { pattern: '**/?(*.)+(spec|test).[tj]s?(x)', ignore: false, trigger: true, load: true, test: true, order: 3 }
    ],
    runAllTestsInAffectedTestFile: false,
    updateNoMoreThanOneSnapshotPerTestFileRun: false,
    addModifiedTestFileToExclusiveTestRun: true,
    compilers: {},
    preprocessors: {},
    maxConsoleMessagesPerTest: 100,
    autoConsoleLog: true,
    delays: { run: 0, edit: 100, update: 0 },
    workers: { initial: 0, regular: 0, recycle: false },
    teardown: undefined,
    hints: {
      ignoreCoverage: '__REGEXP /ignore coverage|istanbul ignore/',
      ignoreCoverageForFile: '__REGEXP /ignore file coverage/',
      commentAutoLog: '?',
      testFileSelection: { include: '__REGEXP /file\\.only/', exclude: '__REGEXP /file\\.skip/' }
    },
    automaticTestFileSelection: true,
    runSelectedTestsOnly: false,
    extensions: {},
    env: {
      type: 'node',
      params: {},
      runner: '<homeDir>/.nvm/versions/node/v14.13.0/bin/node',
      viewportSize: { width: 800, height: 600 },
      options: { width: 800, height: 600 },
      bundle: true
    },
    reportUnhandledPromises: true,
    slowTestThreshold: 75,
    lowCoverageThreshold: 80,
    loose: true,
    configCode: 'auto.detect#-1295911054'
  },
  packageJSON: {
    dependencies: {
      '@angular/animations': '^11.2.0',
      '@angular/common': '^11.2.0',
      '@angular/compiler': '^11.2.0',
      '@angular/core': '^11.2.0',
      '@angular/forms': '^11.2.0',
      '@angular/platform-browser': '^11.2.0',
      '@angular/platform-browser-dynamic': '^11.2.0',
      '@angular/router': '^11.2.0',
      '@nrwl/angular': '11.3.1',
      rxjs: '~6.6.3',
      tslib: '^2.0.0',
      'zone.js': '^0.10.2'
    },
    devDependencies: {
      '@angular-devkit/build-angular': '~0.1102.0',
      '@angular-eslint/eslint-plugin': '~1.0.0',
      '@angular-eslint/eslint-plugin-template': '~1.0.0',
      '@angular-eslint/template-parser': '~1.0.0',
      '@angular/cli': '~11.0.0',
      '@angular/compiler-cli': '^11.2.0',
      '@angular/language-service': '^11.2.0',
      '@nrwl/cli': '11.3.1',
      '@nrwl/cypress': '11.3.1',
      '@nrwl/eslint-plugin-nx': '11.3.1',
      '@nrwl/jest': '11.3.1',
      '@nrwl/linter': '11.3.1',
      '@nrwl/tao': '11.3.1',
      '@nrwl/workspace': '11.3.1',
      '@types/jest': '26.0.8',
      '@types/jasmine': '~3.5.0',
      '@types/node': '12.12.38',
      '@typescript-eslint/eslint-plugin': '4.3.0',
      '@typescript-eslint/parser': '4.3.0',
      cypress: '^6.0.1',
      dotenv: '6.2.0',
      eslint: '7.10.0',
      'eslint-config-prettier': '6.0.0',
      'eslint-plugin-cypress': '^2.10.3',
      'jasmine-core': '~3.6.0',
      'jasmine-spec-reporter': '~5.0.0',
      karma: '~5.0.0',
      'karma-chrome-launcher': '~3.1.0',
      'karma-coverage-istanbul-reporter': '~3.0.2',
      'karma-jasmine': '~4.0.0',
      'karma-jasmine-html-reporter': '^1.5.0',
      jest: '26.2.2',
      'jest-preset-angular': '8.3.2',
      prettier: '2.2.1',
      'ts-jest': '26.4.0',
      'ts-node': '~9.1.1',
      typescript: '~4.0.3'
    }
  },
  fs: { numberOfFiles: 42 },
  debug: [
    '2021-02-24T11:44:20.677Z angular/cli config Detected Angular CLI.\n',
    '2021-02-24T11:44:20.678Z angular/cli config @nrwl/workspace v11.1.4 and higher uses jest automatic configuration.\n',
    '2021-02-24T11:44:20.731Z jest/config Detected Jest.\n',
    '2021-02-24T11:44:20.732Z jest/config Configured Jest.\n',
    '2021-02-24T11:44:20.733Z project Wallaby Node version: v14.13.0\n',
    '2021-02-24T11:44:20.733Z project Wallaby config: <homeDir>/Developer/remove-me/auto.detect\n',
    '2021-02-24T11:44:20.866Z project File cache: <homeDir>/.vscode/extensions/wallabyjs.wallaby-vscode-1.0.268/projects/32dcc9439bf4d5db\n',
    '2021-02-24T11:44:20.928Z uiService Listening port 51235\n',
    '2021-02-24T11:44:20.940Z workers Parallelism for initial run: 10, for regular run: 5\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #0\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #1\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #2\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #3\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #4\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #5\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #6\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #7\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #8\n',
    '2021-02-24T11:44:20.940Z workers Starting run worker instance #9\n',
    '2021-02-24T11:44:20.941Z workers Web server is listening at 54677\n',
    '2021-02-24T11:44:23.857Z project File cache requires some updates, waiting required files from IDE\n',
    '2021-02-24T11:44:23.877Z workers Started run worker instance (delayed) #1\n',
    '2021-02-24T11:44:23.877Z workers Started run worker instance (delayed) #4\n',
    '2021-02-24T11:44:23.877Z workers Started run worker instance (delayed) #2\n',
    '2021-02-24T11:44:23.877Z workers Started run worker instance (delayed) #3\n',
    '2021-02-24T11:44:23.878Z workers Started run worker instance (delayed) #5\n',
    '2021-02-24T11:44:23.878Z workers Started run worker instance (delayed) #6\n',
    '2021-02-24T11:44:23.879Z workers Started run worker instance (delayed) #7\n',
    '2021-02-24T11:44:23.879Z workers Started run worker instance (delayed) #8\n',
    '2021-02-24T11:44:23.880Z workers Started run worker instance (delayed) #0\n',
    '2021-02-24T11:44:23.883Z project Stopping process pool\n',
    '2021-02-24T11:44:23.886Z project Test run started; run priority: 3\n',
    '2021-02-24T11:44:23.887Z project Running all tests\n',
    '2021-02-24T11:44:23.889Z workers Starting test run, priority: 3\n',
    '2021-02-24T11:44:23.889Z workers Distributing tests between 10 workers\n',
    '2021-02-24T11:44:23.889Z workers Running tests in parallel\n',
    '2021-02-24T11:44:23.890Z nodeRunner Starting sandbox [worker #0, session #zt1us]\n',
    '2021-02-24T11:44:23.890Z nodeRunner Starting sandbox [worker #1, session #qqq2h]\n',
    '2021-02-24T11:44:23.890Z nodeRunner Preparing sandbox [worker #0, session #zt1us]\n',
    '2021-02-24T11:44:23.890Z nodeRunner Preparing sandbox [worker #1, session #qqq2h]\n',
    '2021-02-24T11:44:23.890Z nodeRunner Prepared sandbox [worker #0, session #zt1us]\n',
    '2021-02-24T11:44:23.890Z nodeRunner Prepared sandbox [worker #1, session #qqq2h]\n',
    '2021-02-24T11:44:23.890Z workers [worker #0, session #zt1us] Running tests in sandbox\n',
    '2021-02-24T11:44:23.891Z workers [worker #1, session #qqq2h] Running tests in sandbox\n',
    '2021-02-24T11:44:23.984Z workers Started run worker instance (delayed) #9\n',
    '2021-02-24T11:44:25.647Z workers Scheduling Jest Test Run: 2021-02-24T11:44:24.870Z\n',
    '2021-02-24T11:44:25.649Z workers Sandbox (active) [zt1us] error: Cannot use import statement outside a module\n',
    '2021-02-24T11:44:25.650Z workers [zt1us] Run 0 test(s), skipped 0 test(s)\n',
    '2021-02-24T11:44:25.651Z workers Jest Test Run Complete: 2021-02-24T11:44:25.645Z\n',
    '2021-02-24T11:44:25.651Z workers [zt1us] Sandbox is responsive, closing it\n',
    '2021-02-24T11:44:25.930Z workers Scheduling Jest Test Run: 2021-02-24T11:44:24.871Z\n',
    '2021-02-24T11:44:25.932Z workers Sandbox (active) [qqq2h] error: <homeDir>/Developer/remove-me/apps/m3-client/src/test.ts: Missing semicolon (10:7)\n' +
      '\n' +
      "   8 | } from '@angular/platform-browser-dynamic/testing';\n" +
      '   9 |\n' +
      '> 10 | declare const require: any;\n' +
      '     |        ^\n' +
      '  11 |\n' +
      '  12 | // First, initialize the Angular testing environment.\n' +
      '  13 | getTestBed().initTestEnvironment(\n',
    '2021-02-24T11:44:25.932Z workers [qqq2h] Run 0 test(s), skipped 0 test(s)\n',
    '2021-02-24T11:44:25.933Z workers Jest Test Run Complete: 2021-02-24T11:44:25.928Z\n',
    '2021-02-24T11:44:25.934Z workers [qqq2h] Sandbox is responsive, closing it\n',
    '2021-02-24T11:44:25.935Z workers Failed to map the stack to user code, entry message: <homeDir>/Developer/remove-me/apps/m3-client/src/test.ts: Missing semicolon (10:7)\n' +
      '\n' +
      "   8 | } from '@angular/platform-browser-dynamic/testing';\n" +
      '   9 |\n' +
      '> 10 | declare const require: any;\n' +
      '     |        ^\n' +
      '  11 |\n' +
      '  12 | // First, initialize the Angular testing environment.\n' +
      '  13 | getTestBed().initTestEnvironment(, stack: SyntaxError: <homeDir>/Developer/remove-me/apps/m3-client/src/test.ts: Missing semicolon (10:7)\n' +
      '\n' +
      "   8 | } from '@angular/platform-browser-dynamic/testing';\n" +
      '   9 |\n' +
      '> 10 | declare const require: any;\n' +
      '     |        ^\n' +
      '  11 |\n' +
      '  12 | // First, initialize the Angular testing environment.\n' +
      '  13 | getTestBed().initTestEnvironment(\n' +
      '    at Parser._raise (<homeDir>/Developer/remove-me/node_modules/@babel/parser/src/parser/error.js:97:45)\n' +
      '    at Parser.raiseWithData (<homeDir>/Developer/remove-me/node_modules/@babel/parser/src/parser/error.js:92:17)\n' +
      '    at Parser.raise (<homeDir>/Developer/remove-me/node_modules/@babel/parser/src/parser/error.js:41:17)\n' +
      '    at Parser.semicolon (<homeDir>/Developer/remove-me/node_modules/@babel/parser/src/parser/util.js:131:10)\n' +
      '    at Parser.parseExpressionStatement (<homeDir>/Developer/remove-me/node_modules/@babel/parser/src/parser/statement.js:805:10)\n' +
      '    at Parser.parseStatementContent (<homeDir>/Developer/remove-me/node_modu\n',
    '2021-02-24T11:44:25.935Z workers Merging parallel test run results\n',
    '2021-02-24T11:44:25.935Z project Test run finished\n',
    '2021-02-24T11:44:25.936Z project Processed console.log entries\n',
    '2021-02-24T11:44:25.936Z project Processed loading sequences\n',
    '2021-02-24T11:44:25.936Z project Processed executed tests\n',
    '2021-02-24T11:44:25.936Z project Processed code coverage\n',
    '2021-02-24T11:44:25.941Z project Test run result processed and sent to IDE\n'
  ]
}
```
