# Google App Script

## Documentation

You can directly go to the [landing page](https://developers.google.com/apps-script/?hl=en). Then you can find to important parts:
- [References](https://developers.google.com/apps-script/reference/) : This is the API
- [Guides](https://developers.google.com/apps-script/overview) : Tutorials 

## First code

You have two options.

- First option. Open a Google Doc (Spreadsheet, Doc or Slides), `Tools > Script Editor`. This will be a Google App Script Project linked to this document.

- Second option. Once inside Google Drive create a Google App Script file. Before you'll need to install Google App Script application. It's easy. `New > More > Connect` more apps. Search "Google App Script" and install it. After that you can create files with `New > More > Google App Script`.  

## Debug 

Let's use the second option to create a GAP inside a Google Spreadsheet (second option).

You will see below de menu (File, ... ) a bunch of buttons. We'll use `Play` and the `Select Box` where you'll find all the functions in the file. `Play` will execute the function selected in the `Select Box`. 

Instead of using ``console.log(...)`` you can create a Log using ``Logger.log()``. You can see the result going to ``View > Logs``.  

```javascript
function myFunction() {
  Logger.log("Hi, world");
}
```

## Menu

More information [here](https://developers.google.com/apps-script/guides/menus) in the guide. 

```javascript
var ui = SpreadsheetApp.getUi();
  ui.createMenu("Personal Tools").
  	addItem("First item","myFunction").
  	addToUi();
```	

Useful functions: 

* ``addItem("Name", "functionName")``
* ``addSeparator()``
* ``addSubMenu(ui.createMenu())``


## Triggers 

Try to change the function name we have created for menu's. Use ``onOpen`` to create a trigger. You can see more triggers [here](https://developers.google.com/apps-script/guides/triggers/). 

You can access to your triggers (inside your GAP file) going to  ``Resources > Current Project's Triggers``.

## SpreadsheetApp

Let's see some of the main functions. All this classes have a hierarchy like this:

```
SpreadsheetApp
|- Spreadsheet
	|- Sheet
		|- Range
```

Let's use [this table](https://docs.google.com/spreadsheets/d/106yf8hGzn6X4KUjclueXAdFd87HlMVwQ1EMb6mfIxxQ/edit?usp=sharing) as a demo.  

