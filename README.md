# Github-Contribution-Graph
Jquery plugin to render like contribution graph on Github when you view user's profile, You can use it to apply on other JS framework like Angularjs as well. 

## DEMO LINK

[DEMO LINK](http://bachvtuan.github.io/Github-Contribution-Graph/)

## Requirements

Jquery library

## Usage:
Add below code into your html content

```html
<script type="text/javascript" src="js/github_contribution.js"></script>
<link href="css/github_contribution_graph.css" media="all" rel="stylesheet" />
```

Create div to render graph

```html
<div id="your_graph"></div>

```

Call lib to render graph

```js
$('#your_graph').github_graph( {
  // Default is null will display date before 365 days from now
  start_date: Date Time object
  //Default is empty list
  data: list_of_timestamp ,
  // single text and plural text
  texts: ['completed task','completed tasks']
});

```
Full options

```js
$('#your_graph').github_graph( {
  // start from 2022, null is default
  start_date: new Date(2022,00,00,0,0,0),
  data: list_of_timestamp ,
  // single text and plural text
  texts: ['category','categories'],
  //Override month names
  month_names: ['T1','T2','T3','T4','T5','T6','T7','T8','T9','T10','T11','T12'],
  //Override horizontal day name
  h_days:['2','4','6'],
  //override colours
  colors:['gray','purple','yellow','green','red'],
  /** List object of color and count also supported
  colors:[
    { count:0, color:'gray' },
    { count:5, color:'purple' },
    { count:10, color:'yellow' },
    { count:15, color:'green' },
    { count:20, color:'red' }
  ],
  **/
  border:{
    radius: 5,
    hover_color: "red"
  },
  click: function(date, count) {
    console.log(date, count);
  },
});
```

Data format: Supported list of timestamp array or object({timestamp,count}).

```js
var list_of_timestamp = [1624865396654,1624865396655, ...];

// or 
var list_of_timestamp = [
  {
    timestamp: 1624865396654,
    count: 2
  },
  {
    timestamp: 1624865396655,
    count: 5
  }
];


```