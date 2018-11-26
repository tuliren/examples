## Fleet plan endpoint example JSON requests

To execute any of these calls, you can use `curl`, specifying your API key and example JSON file.
```
curl -X POST \
  -H "Content-Type: application/json" \
  -H "X-Api-Key: <YOUR_KEY>" \
  -d @<JSON_FILE> \
  https://api.rideos.ai/fleet/v2/GetPlan
```

### List of available examples
* `simplePlan.json`
  * Get a plan for a single vehicle with a single pickup/dropoff task in the area
* `oneVehicleMultipleTasks.json`
  * Get a plan for a single vehicle servicing multiple pickups and dropoffs
* `multipleVehiclesMultipleTasks.json`
  * Get a plan for multiple vehicles servicing multiple pickups and dropoffs around the area
* `vehiclesAlreadyAssignedTasks.json`
  * Get a plan for multiple vehicles and multiple tasks when some of the vehicles are already in the process of
  servicing existing tasks
