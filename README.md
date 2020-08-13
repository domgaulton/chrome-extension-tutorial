# Chrome Plugin

* https://developer.chrome.com/extensions/getstarted

1. Your manifest.json controls everything to do with the plugin
2. The background manages the background action of your plugin / function
```json
"background": {
	"scripts": ["background.js"],
	"persistent": false
},
```
3. Within `background.js` the urls can be set and the action the plugin is active is set with 
```js
actions: [new chrome.declarativeContent.ShowPageAction()]
```
4. Show Page Action runs the manifest function `page_action` which shows the `popup.html` upon click
```json
"page_action": {
  "default_popup": "popup.html",
  "default_icon": {
    "16": "images/get_started16.png",
    "32": "images/get_started32.png",
    "48": "images/get_started48.png",
    "128": "images/get_started128.png"
  }
},
```