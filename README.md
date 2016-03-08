# bower-jquery-selection

## About

This project is a bower friendly version of [jQuery.selection](https://github.com/madapaja/jquery.selection) plugin.


# Installing

## Bower

```bash
    bower install bower-jquery-selection
```

```html
    <script src="bower_components/bower-jquery-selection/src/jquery.selection.js"></script>
```

# Examples

## AngularJS

```html
<div ng-controller="SelectionController as selection">
    <p>
        <button ng-click="selection.onClick()">Get selected text</button>
        <input type="text" id="input" value="This is an AngularJS integration example" class="col-md-4"/><br/>
    </p>
</div>
```

```javascript
angular.module('myProjectApp')
    .controller('SelectionController', function () {
        var vm = this;
        vm.onClick = function () {
            var input = angular.element('#input');
            alert(input.selection());
            input.focus();
        };
    });
```

## jQuery

```html
<div>
    <p>
        <button id="button">Get selected text</button>
        <input type="text" id="input" value="This is a jquery integration example" class="col-md-4"/><br/>
    </p>
</div>
```

```javascript
$('#button').click(function () {
    alert($('#input').selection());
    $('#input').focus();
});
```

To see more details and examples, please go to [jQuery.selection website](http://madapaja.github.io/jquery.selection/)