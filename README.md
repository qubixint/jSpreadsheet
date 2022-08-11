# Jspreadsheet CE v4: The JavaScript spreadsheet for Angular

[**Jspreadsheet CE**](https://bossanova.uk/jspreadsheet/v4/) is a lightweight Vanilla JavaScript plugin to create amazing web-based interactive HTML tables and spreadsheets compatible
with other spreadsheet software. You can create an online spreadsheet table from a JS array,
JSON, CSV or XSLX files. You can copy from excel and paste straight to your Jspreadsheet CE spreadsheet and vice versa.
It is very easy to integrate any third party JavaScript plugins to create your own custom columns, custom editors, and customize any
feature into your application. Jspreadsheet CE has plenty of different input options through its native column types to cover the most common web-based application
requirements. It is a complete solution for web data management. Create amazing applications with Jspreadsheet CE JavaScript spreadsheet.

## Main advantages 
- Make rich and user-friendly web interfaces and applications. 
- You can easily handle complicated data inputs in a way users are used..
- Improve your user software experience.
- Create rich CRUDS and beautiful UI.
- Compatibility with excel: users can move data around with common copy and paste shortcuts.
- Easy customizations with easy third-party plugin integrations.
- Lean, fast and simple to use.
- Thousands of successful user cases.
- Speed up your work dealing with difficult data entry in a web-based software.

## Screenshot
![The JavaScript spreadsheet](https://bossanova.uk/templates/default/img/jexcel.gif)

## Basic demo 
A basic example to integrate the JavaScript spreadsheet in your website to create your first online spreadsheet. <https://codepen.io/hchiam/pen/qBRzXKK>

## News
- <b>Important</b>: Please import jspreadsheet.css (jexcel.css is not longer available in this package).
- Please use Jsuites v4
- New mask system (https://jsfiddle.net/spreadsheet/vmjo34r8/)

# Installation and usage

### Install using npm (node package manager)

Add this line to the package.json file

```package.json
"dependencies": {
    "jspreadsheet-ce": "git+https://github.com/eXamqle/jSpreadsheet-ce-Qubix-International.git"
},
  "devDependencies": {
    "@types/jspreadsheet-ce": "^4.7.3"
}
```

> `npm install`

### Or using standalone library/js plugin

[Download ZIP](https://github.com/jspreadsheet/ce/archive/master.zip) and and then use the files of `dist` folder in your project (js library and css files)

## Usage
  
### Add jexcel/jspreadsheet and jsuites styles to Angular *index.html* file
```index.html
<link rel="stylesheet" href="https://jsuites.net/v4/jsuites.css" type="text/css" />
<link rel="stylesheet" href="https://bossanova.uk/jspreadsheet/v4/jexcel.css" type="text/css" />
```
### Or download and declare jexcel/jspreadsheet styles and jsuites to *angular.json* file


<ol>
  <li>jSuites CSS File: https://jsuites.net/v4/jsuites.css</li>
  <li>jExcel CSS File: https://bossanova.uk/jspreadsheet/v4/jexcel.css</li>
</ol>

```
"styles": [
    "src/theme/default.scss",
    "src/styles.scss",
    "src/themes/jsuites.scss", <-- Rename .css to .scss
    "src/themes/jexcel.scss"   <-- Rename .css to .scss
]
```
Then initialize your table based on a div container, such as:
```jspreadsheet.component.html
<div #spreadsheet></div>
```
To initialize a Jspreadsheet CE table you should run TypeScript, such as:
```jspreadhseet.component.ts

export class SpreadsheetComponent {

@ViewChild("spreadsheet") spreadsheet!: ElementRef;
  title = "CodeSandbox";

  ngAfterViewInit() {
    jspreadsheet(this.spreadsheet.nativeElement, {
      data: [[]],
      columns: [
        { type: "dropdown", source: ["Y", "N"] },
        { type: "color", render: "square" }
      ],
      minDimensions: [10, 10]
    },);
  }
}

```
# Jspreadsheet CE History
### Jspreadsheet CE 4.6
<b>Jexcel</b> has been renamed to <b>Jspreadsheet</b>
### Jspreadsheet CE 4.0.0
A special thank to the [FDL - Fonds de Dotation du Libre](https://www.fdl-lef.org/) support and sponsorship that make this version possible with so many nice features.
- Support workbooks/tabs
- Create a dymic jexcel table from a HTML static element
- Highlight the border from cells after CTRL+C
- Footer with formula support
- Multiple columns resize
- JSON update support (Helpers to update a remote server)
- Global super event (centralized method to dispatch all events in one)
- Custom helpers: =PROGRESS (progressbar), =RATING (5 star rating)
- Custom helpers: =COLUMN, =ROW, =CELL, =TABLE, =VALUE information to be used on formula execution
- Dynamic nested header updates
- A new column type for HTML editing
- New flags such as: includeHeadersOnCopy, persistance, filters, autoCasting, freezeColumns
- New events such as: onevent, onchangepage, onbeforesave, onsave
- More examples and documentation
## Official website
- [Jspreadsheet CE v4 - Javascript Spreadsheet](https://bossanova.uk/jspreadsheet/v4)
## Community
- [GitHub](https://github.com/jspreadsheet/ce/issues)
## Copyright and license
Jspreadsheet CE is released under the [MIT license]. Contact <contact@jspreadsheet.com>
## Other interesting tools
- [jSuites - JavaScript plugins & Webcomponents](https://jsuites.net)
- [Jspreadsheet Pro](https://jspreadsheet.com)
- [LemonadeJS Reactive Library](https://lemonadejs.net)
