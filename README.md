# ng-Grid Mouse Events

This simple plugin for ng-grid allows you to bind multiple mouse events (`onClick`, `onDblClick`, `onRightClick`) to rows.

## Usage
Include the plugin in the grid options, and the binding methods become available

```html
<script type="text/javascript" src="angular.js"></script>
<script type="text/javascript" src="ng-grid.js"></script>
<script type="text/javascript" src="ng-grid-mouse-events.js"</script>
<script>
  angular.module('myApp', ['ngGrid']);
</script>
<body ng-app="myApp">
  <div ng-grid="myOptions"></div>
</body>
```

#### In your controller:
```javascript
function MyCtrl($scope) {
  $scope.myOptions = {
    onClick: function(row) {
      // Row was clicked
    },
    onRightClick: function(row) {
      // Row was right-clicked
    },
    onDblClick: function(row) {
      // Row was double clicked
    }
  }
}
```
