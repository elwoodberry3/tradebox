# Errors
Roadblocks that occured during the development of this project  




Update Packager command for IOS OS
```
"package": "electron-packager ./dist/tradebox TradeBox --platform=darwin --arch=universal"
```


## File Size  
Troubleshoot the following error wht the directory does not exist.
```
remote: error: File tradebox/TradeBox-darwin-universal/TradeBox.app/Contents/Frameworks/Electron Framework.framework/Versions/A/Electron Framework is 314.07 MB; this exceeds GitHub's file size limit of 100.00 MB
```

## Browser Warning
Trouble shoot the following warning:
```
node:electron/js2c/renderer_init:2 Electron Security Warning (Insecure Content-Security-Policy) This renderer process has either no Content Security
  Policy set or a policy with "unsafe-eval" enabled. This exposes users of
  this app to unnecessary security risks.

For more information and help, consult
https://electronjs.org/docs/tutorial/security.
This warning will not show up
once the app is packaged.
```  

## Path Error  
```  
Not allowed to load local resource: file:///Users/adbyrd/Documents/github/tradebox/tradebox/dist/tradebox/index.html  
```  


## Package Path Error  
Error occured when trying to package the application.  
```
Troubleshoot the following error:
ENOENT: no such file or directory, stat './tradebox'
```
The true path in the package.json should be ""package": "electron-packager ./dist/tradebox TradeBox --platform=win32 --arch=x64""



## Manifest Not Found
Error occured when trying to package the application.  
```
Application manifest was not found. Make sure "dist/tradebox/package.json" exists and does not get ignored by your ignore option
```  
Copied the package.json file to the 'dist/tradebox' directory



## Entry Point
Troubleshoot the following
Error occured when trying to package the application. 
```
The main entry point to your app was not found. Make sure "dist/tradebox/index.js" exists and does not get ignored by your ignore option
```  
