
TOC
[Installation](#installation)

# Installation
## Node.js
* Install latest Node.js
* Install or update latest NPM
* Install Bower
* Install Cordova
* Install Ionic (beta for version 2)
* Install node-gyp latest
* Config parameters ```npm config ... -g``` globally
 * Python
 * MSVC environment
## Frameworks
* Install cordova, ionic, bower globally
* Update cordova for all platforms
 * ```cordova platform update android```

## Ionic
* Download and install Ionic Lab
* Link the ionic lab to your account

# Setup
## Android
* Install Studio and SDK
* Update SDKs and tools
 * e.g. Extras->IntelHAXM
* Install x86 images for all android versions
* Post install set environment variables
 * ```ANDROID_HOME``` where the SDK is placed
 * Put ```ANDROID_HOME``` and ```ANDROID_HOME\tools``` in ```PATH```  
* after you install ```HAXM installer``` from extras run ```{SDK_FOLDER}\extras\intel\Hardware_Accelerated_Execution_Manager\intelhaxm-android.exe.exe```
* Create an AVD with x86 and set characteristics
* Intstead of launching with ionic, do it with ```cordova emulate --emulator=thenameofthedevice android```

## Windows
* Install Windows 10 SDK **Important**
* Install Visual Studio build tools 2015 **with cross platform tools**
* Check that python is in your path by writting python --version in the console. If not then
 * Download python 2.7 (I recommend chocolatey (choco install python2 -y))
* Check that you have .NET 4.5.1+ installed. If not then *Download and install .NET 4.5.1 (.NET 4.5.2 will also work just fine*
* Download Microsoft Visual C++ Build Tools 2015 Technical Preview 
* Set the npm config variable msvs_version to 2015: npm config -g set msvs_version 2015
* Do npm i in what-ever project with node-gyp as a dependency without seeing weird error messages :+1:

Tested with node 5.0.0+ and npm 3.3.6

# IDE
* Use Visual Studio Community 2015
* After installation (or during if you use the advance mode) install ```cross platform development tools```
* Also install Ionic 2 Templates, Web Kit, ...
* Open folder and work

# Ionic
## Platform specific customization
Read more: http://ionicframework.com/docs/platform-customization/dynamic-templates.html

##Application Structure
http://ionicframework.com/docs/concepts/structure.html

* ```app```: 

# Other Tools
* SQlite studio (http://sqlitestudio.pl/?act=download)

# Templates
# Package.json
```
{
  "name": "cross-platform-template",
  "version": "1.1.1",
  "description": "cross-platform-template: An Ionic project",
  "dependencies": {
    "@angular/common": "^2.0.0-rc.4",
    "@angular/compiler": "^2.0.0-rc.4",
    "@angular/core": "^2.0.0-rc.4",
    "@angular/forms": "^0.2.0",
    "@angular/http": "^2.0.0-rc.4",
    "@angular/platform-browser": "^2.0.0-rc.4",
    "@angular/platform-browser-dynamic": "^2.0.0-rc.4",
    "angular2": "^2.0.0-beta.17",
    "colors": "^1.1.2",
    "del": "^2.2.1",
    "es6-shim": "^0.35.0",
    "gulp": "^3.5.6",
    "gulp-concat": "^2.2.0",
    "gulp-minify-css": "^0.3.0",
    "gulp-rename": "^1.2.0",
    "gulp-sass": "^2.0.4",
    "gulp-watch": "^4.3.9",
    "inquirer": "0.11.0",
    "ionic-angular": "^2.0.0-beta.10",
    "ionic-gulp-browserify-typescript": "^2.0.0",
    "ionic-gulp-fonts-copy": "^1.0.0",
    "ionic-gulp-html-copy": "^1.0.0",
    "ionic-gulp-sass-build": "^1.0.0",
    "ionic-gulp-scripts-copy": "^2.0.1",
    "ionic-gulp-tslint": "^1.1.0",
    "ionic-native": "^1.3.10",
    "ionicons": "3.0.0",
    "lodash": "4.14.1",
    "mkdirp-no-bin": "0.5.1",
    "q": "1.4.1",
    "reflect-metadata": "^0.1.2",
    "run-sequence": "^1.2.2",
    "rxjs": "5.0.0-beta.6",
    "zone.js": "^0.6.12"
  },
  "devDependencies": {
    "bower": "^1.3.3",
    "gulp-util": "^2.2.14",
    "shelljs": "^0.3.0"
  },
  "cordovaPlugins": [
    "cordova-plugin-device",
    "cordova-plugin-console",
    "cordova-plugin-whitelist",
    "cordova-plugin-splashscreen",
    "cordova-plugin-statusbar",
    "ionic-plugin-keyboard"
  ],
  "cordovaPlatforms": []
}
```