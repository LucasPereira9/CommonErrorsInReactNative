# common errors in react native

*Hello, my name is Lucas and in this repository I will list some of the common errors that I face most in my day to day working with react native. I will always update so that I can help myself and also help everyone who has problems with this language.*



***my linkedIn page*** [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/lucas-pereira-5280b9206/)](https://www.linkedin.com/in/lucas-pereira-5280b9206/)




![This is an image](https://github.com/LucasPereira9/Erros-Comuns-React-Native/blob/main/assets/react-native.jpg)   


## Error: listen EADDRINUSE :::8081
When this error occurs, it means that port 8081 is already being used. There is probably already some terminal running the Metro Bundler of your project, just close it and try again. However, if you don't find this process running, you can end it manually with the following command:

 ```taskkill /f /im node.exe```  // for windows
 
 ```pkill node``` // for linux and MacOS
 
 
## The development server returned response error code: 500
Usually this error happens when you try to import a JS file that doesn't have export defaultor doesn't have any components inside it.

First check all recent files and imports you've done to make sure they all have import/exports and their components.

If that doesn't work, close the Metro Bundler terminal window that opens automatically with run-ios/run-androidand in your project folder run:

```npx react-native start --reset-cache```

or ```yarn run react-native start --reset-cache```

or ```yarn start --reset-cache```

which command to use will depend on the situation.




## internal/modules/cjs/loader.js ... throw error cannot find module ...
If you get such an error, check that your project path is a valid path. It is not a valid path if it contains space or special characters. Examples:

> c:/folder with space/project     ## invalid path

> c:/perfectCafé/project    ## invalid path

> c:/components/header/index.js    ## valid path
