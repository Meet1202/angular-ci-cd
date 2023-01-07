## Recommended packages and configuration for angular to check ```Lint```, ```Testcase``` and ```Deploy in Github-pages``` in CI/CD.

Angular Version: v15.0.0
Node Version: v18.13.0
### Install Es Lint according to your angular version
    CMD: ng add @angular-eslint/schematics

### Install  puppeteer for chromeHeadeless for testing
    npm install puppeteer --save-dev
    
### In karma.conf.js under restartOnFileChange: true, add below code
            customLaunchers: {
                ChromeHeadlessCustom: {
                    base: 'ChromeHeadless',
                    flags: ['--no-sandbox', '--disable-gpu']
                }
            }
            
### In package.json update test script
    "test": "ng test --watch=false --browsers=ChromeHeadlessCustom",

### To Deploy in Github page
    ng add angular-cli-ghpages
    ng deploy --base-href=/<repo-name>/
    
