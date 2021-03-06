# angular-money-mask


### AngularJS Native Money Mask

This directive relies on the AngularJS currency filter in order to transform the number into currency. You may import the i18n locale to apply it to your local currency.

#### Configuration

Step 1: Importing the money-mask module to your application

```
angular.module("yourAppName", "money-mask");
```

Step 2: Using the directive

```
<input type="text" ng-model="value" money-mask/>
```

Step 3: Enjoy!

#### Example

```
<!DOCTYPE html>
<html ng-app="money-mask-example">
<head>
	<title>Money Mask Example</title>
	<script src="lib/angular.js"></script>
	<script src="lib/angular-money-mask.js"></script>
	<script>
		angular.module("money-mask-example", ["money-mask"]);
		angular.module("money-mask-example").controller("exampleController", function ($scope) {
			$scope.value = "$10.00";
		});
	</script>
</head>
<body ng-controller="exampleController">
	real value = {{value}}<br/>
	<input type="text" ng-model="value" money-mask/><br/>
</body>
</html>
```

