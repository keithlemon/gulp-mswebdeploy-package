# gulp-mswebdeploy-package

> Create Microsoft(TM) Web Deploy Packages With Gulp on Any Platform

## Introduction
gulp-mswebdeploy-package allows you to bundle you site file into a Microsoft(TM) compatible web deploy file that can be used to publish to IIS. It is useful for creating build for JavaScript \ HTML project that are built and publish with Visual Studio Online, Visual Studio Team Services, TFS or and system that supports Web Deploy. Please note this package DOES NOT DO THE ACTUAL DEPLOYMENT it simply creates the package.

## Getting Started


```shell
npm install gulp-mswebdeploy-package --save-dev
```


## Using the "mswebdeploy" task

```js

    var mswebdeploy = require('gulp-mswebdeploy');

    gulp.task('package', function(){
        gulp.src('app/')
        .pipe( mswebdeploy({ 'source' : 'app', "dest" : "deploy", 'website': 'Default Web Site' }) )
        .pipe( gulp.dest('/deploy') );
    });

```


This sample creates a web deploy package using the files in 'app' in a folder called 'deploy' in a package named 'webdeploy.zip' The folder structure of the source folder will be maintained in the package. The destination site is optional, and will be set to the same source if nothing is specified (website parameter).
There is currently no way to add individual files.



## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Mocha](https://mochajs.org/).

## Release History
0.1.0 : Beta Release
0.1.2 : Updated docs
0.1.3 : Updated package.json
0.1.4 : Added the website parameter


# gulp-mswebdeploy-package
