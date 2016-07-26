# AngularJS Samples

list:

 * Table: Dynamic Columns and Ordering



```javascript
<ul sortable-list class="sortable">
	<li class="ui-state-default" ng-repeat="column in columns">
		<input type="checkbox" ng-model="column.checked">
		{{column.display}}
	</li>
</ul>
```
