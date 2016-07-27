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

```javascript
<div class="table-responsive">
	<table class="table table-bordered table-striped table-hover table-condensed">
		<thead>
			<tr>
				<th ng-repeat="column in columns | filter: { 'checked': true} | orderBy: 'order'">
					{{column.display}}
				</th>
			</tr>
		</thead>
		<tbody>
			<tr ng-repeat="agent in agents">
				<td ng-repeat="column in columns" ng-if="column.checked">
					{{ getCellValue(agent, column) }}
				</td>
			</tr>
		</tbody>
	</table>
</div>
```
