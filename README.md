# RggD9 Discord Client  
A Discord client written in C++.  

WebView2 is used as the web browser (Microsoft Edge, Windows 10+).  

### Features  
- Supports running in the background.  
- Can execute custom JavaScript files.   

### Preview  
![Main window](preview/preview1.PNG)

![Main window with console](preview/preview2.PNG)  

![Tray icon menu](preview/preview3.PNG)

![Console logs](preview/preview4.PNG)  

# Installation  

### Requirements  
- Windows 10 or newer  
- WebView2 Runtime (automatically installed on most modern systems)  

### How to Install  
1. Download the latest version of **RggD9 Discord Client**.  
2. Move the files to your preferred location.  
3. Run `RggD9-Discord-Client.exe`.  

### First Launch  
- The program will generate a `config.cfg` file if it does not already exist.  
- The default data folder will be created based on the generated configuration.  

### WebView2 Installation (If Needed)  
If the client fails to start due to a missing WebView2 component, you can install it manually:  
- Download WebView2 Runtime from [Microsoft's official website](https://developer.microsoft.com/en-us/microsoft-edge/webview2/).  
- Install it and restart the client.  

## Customization  
This client can be customized via the `config.cfg` file.  
### config.cfg:
```json
{
    "ver": 1.0,
    "useAppDataForData": false,
    "customDataFolder": ".\\RggD9 Discord Client",
    "useCustomScripts": true,
    "ShowConsole": false,
    "pauseOnExit": false,
    "screen": {
        "sizeX": 1280,
        "sizeY": 720
    }
}
```
### Parameter Description  
| Key                  | Type    | Description |
|----------------------|--------|-------------|
| **ver**             | double | Configuration version. If the value is higher than the program version, an error may occur. |
| **useAppDataForData** | boolean | If `true`, WebView2 data will be stored in `%appdata%`. |
| **customDataFolder** | string  | If `useAppDataForData` is `false`, specifies the folder for WebView2 data. |
| **useCustomScripts** | boolean | If `true`, the client will load custom JS scripts from `"customDataFolder\script"`. |
| **ShowConsole**      | boolean | If `true`, the client will display a console for logs. If `false`, logs will be saved in `"customDataFolder\logs\log-%date%.log"`. |
| **pauseOnExit**      | boolean | If `true`, the program will pause in the console (only if `ShowConsole` is `true`). |
| **screen.sizeX**     | int     | Window width in pixels. |
| **screen.sizeY**     | int     | Window height in pixels. |

## Known Issues & Limitations  
- **Requires WebView2** – The client will not work on systems that do not support WebView2 (such as Windows 7).  
- **No built-in update system** – Updates must be downloaded manually.  

## Changelog  
### Version 1.0  
- Initial release of **RggD9 Discord Client**.  
- Simple WebView2-based Discord client.  
- Support for background mode.  
- Ability to load custom JavaScript.  
- Configurable settings via `config.cfg`.  
- Console logging feature with optional log file saving.  

## To-Do  
### Planned Features  
- 🔄 **Auto-update system** 
- 🔄 **Better error handling**
