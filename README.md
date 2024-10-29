# TradeBOX  

NPM  
```  
npm -v
10.8.1
```  
  
Node.js  
```
node --version  
v20.16.0  
```  

Angular CLI
```
ng v  
18.1.4
```

Install Electron  
```  
npm install --save-dev electron
```  
  
Electron  
./electron/main.js  
```js  
const { app, BrowserWindow } = require('electron');
const path = require('path');

let mainWindow;

function createWindow() {
  mainWindow = new BrowserWindow({
    width: 800,
    height: 600,
    webPreferences: {
      nodeIntegration: true,
      contextIsolation: false,
    },
  });

  mainWindow.loadURL(`file://${path.join(__dirname, '../dist/tradebox/index.html')}`);

  mainWindow.on('closed', function () {
    mainWindow = null;
  });
}

app.on('ready', createWindow);

app.on('window-all-closed', function () {
  if (process.platform !== 'darwin') {
    app.quit();
  }
});

app.on('activate', function () {
  if (mainWindow === null) {
    createWindow();
  }
});


```   

Package.json  
```json
  "scripts": {
    "ng": "ng",
    "start": "ng serve",
    "build": "ng build",
    "watch": "ng build --watch --configuration development",
    "test": "ng test",
    "serve:ssr:tradebox": "node dist/tradebox/server/server.mjs",
    "electron": "ng build && electron ./electron/main.js",
    "electron:dev": "ng build --watch & electron ./electron/main.js"
  }
```  

Angular.json  
```json  
"outputPath": "dist/tradebox",
```  

Run Application  
```
npm run electron  
```  
  
Install Packager  
```
npm install --save-dev electron-packager  
```  
  
Update the package.json  
```json  
  "scripts": {
    "package": "electron-packager ./dist/tradebox TradeBox --platform=darwin --arch=universal"
  },
```  

Package the application.
```
npm run package  
```  
