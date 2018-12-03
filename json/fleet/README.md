## Fleet plan endpoint example JSON requests

To execute any of these calls, you can use `curl`, specifying your API key and example JSON file:
```
curl https://api.rideos.ai/fleet/v2/GetPlan \
  -X POST \
  -H "Content-Type: application/json" \
  -H "X-Api-Key: $RIDEOS_API_KEY" \
  -d @JSON_FILE
```

For instance, to execute the `simplePlan.json` request, you'd run:
```
curl https://api.rideos.ai/fleet/v2/GetPlan \
  -X POST \
  -H "Content-Type: application/json" \
  -H "X-Api-Key: $RIDEOS_API_KEY" \
  -d @simplePlan.json
```
Note that this assumes that your API key is stored in the `RIDEOS_API_KEY` environment variable. For instructions on how to obtain an API key, see the [top-level README](https://github.com/rideOS/examples/blob/master/README.md) in this repo.

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
