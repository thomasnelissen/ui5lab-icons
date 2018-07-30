# Use third-party icon fonts in UI5 applications

This library allows you to use third-party icon fonts in your UI5 application. Currently the following icon fonts are supported:
* [Font Awesome](https://fontawesome.com/)
* [Material Design](https://material.io/tools/icons/?style=baseline)

## How to use this library

Use the IconLoader.load API to load icon fonts in your application. You can call this API in the Component.js init function or in a View Controller's onInit function.

```javascript
sap.ui.define([
	"sap/ui/core/mvc/Controller",
	"ui5lab/tn/icons/IconLoader"
], function (Controller, IconLoader) {
	"use strict";
	return Controller.extend("be.tn.IconsDemo.controller.Icons", {
		onInit: function () {
			IconLoader.load("fa"); // Load Font Awesome icon font
			IconLoader.load("md"); // Load Material Design icon font
		}
	});
});
```

When this is done you can use the icons in the following way: sap-icon://<<icon_font_code>>/<<icon_name>>
```xml
<core:Icon src="sap-icon://fa/bicycle" />
<core:Icon src="sap-icon://md/commute" />
```

## Contributing

Contributions are welcomed. Please use a feature branch and don't forget to include your name in the list below.

## Authors

* **Thomas Nelissen** - [TNFlexso](https://github.com/TNFlexso)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
