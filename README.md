# Github-Contribution-Graph
Jquery plugin to render like contribution graph on Github when you view user's profile, You can use it to apply on other JS framework like Angularjs as well. 

## DEMO LINK

[DEMO LINK](http://bachvtuan.github.io/Github-Contribution-Graph/)

## Requirements

Jquery library

## Usage:
Add below code into your html content

```
<script type="text/javascript" src="js/github_contribution.js"></script>
<link href="css/github_contribution_graph.css" media="all" rel="stylesheet" />
```

Create div to render graph

```
<div id="your_graph"></div>

```

Call lib to render graph

```
$('#your_graph').github_graph( {
  //Default is empty list
  data: list_of_timestamp ,
  // single text and plural text
  texts: ['completed task','completed tasks']
});

```
Here is full options

```
$('#your_graph').github_graph( {
  
  data: list_of_timestamp ,
  // single text and plural text
  texts: ['category','categories'],
  //Override month names
  month_names: ['T1','T2','T3','T4','T5','T6','T7','T8','T9','T10','T11','T12'],
  //Override horizontal day name
  h_days:['2','4','6'],
  //override colours
  colors:['gray','purple','yellow','green','red']
});
```