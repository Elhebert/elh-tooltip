# Installation

### Bower
Install the package with: `bower install ng-tooltip` then add the files to your index.html
```
<link rel="stylesheet" href="./bower_components/tooltip.css">

<script src="./bower_components/ng-tooltip/tooltip.js">
```

### npm:
Install the package with: `npm install ng-tooltip` then add the files to your index.html
```
<link rel="stylesheet" href="./node_modules/tooltip.css">

<script src="./nodes_modules/ng-tooltip/tooltip.js">
```

### Manually:
Clone the repository with `git clone https://github.com/Elhebert/ng-tooltip.git` then add the files to your index.html
```
<link rel="stylesheet" href="/path/to/tooltip.css">

<script src="/path/to/ng-tooltip/tooltip.js">
```

# Customisation

### Design
Add the following rules to your scss/sass/css file:

Using sass or scss:
```
[tooltip] {
	// Element for which the tooltip appear
	 .tooltip {
		// Tooltip
		&.active .tooltip {
			//Tooltip when active
		}
	 }
}
```

Using css:
```
[tooltip] {
	// Element for which the tooltip appear
}
[tooltip] .tooltip {
	// Tooltip
}
[tooltip].active .tooltip {
	//Tooltip when active
}
```

### Placement
You can modify the placement of the tooltip by changing the following lines in **tooltip.js**
```
childElement.css({
	top: element[0].offsetTop + (element[0].offsetHeight / 2) + 'px',
	left: element[0].offsetLeft - (childElement[0].offsetWidth / 2) + (element[0].offsetWidth / 2) + 'px',
});
```