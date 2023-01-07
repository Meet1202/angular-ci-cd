## Recommended packages and configuration for angular to check ```Lint```, ```Testcase``` and ```Deploy in Github-pages``` in CI/CD.

## Angular Version: v15.0.0
## Node Version: v18.13.0
### Install Es Lint according to your angular version
    CMD: ng add @angular-eslint/schematics

### In package.json update test script
    "test": "ng test --watch=false --browsers=ChromeHeadless",

### To Deploy in Github page
    ng add angular-cli-ghpages
    ng deploy --base-href=/<repo-name>/
    
