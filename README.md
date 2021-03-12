# Multi instance subprocess with complex object collection

Demonstration using complex objects as process variables in combination with multi instance sub process

> Recommendation is to use JSON to serialize complex objects. More info [here](https://camunda.com/best-practices/handling-data-in-processes/#__strong_serializing_strong_complex_data)

**Account:** admin 
**password:** admin123
---
## Steps
1. start project by executing spring-boot:run
2. login the [tasklist](http://localhost:8080/camunda/app/tasklist/default/#/) 
3. start Car Type process
4. navigate to the [cockpit](http://localhost:8080/camunda/app/cockpit/default/#/)
5. look for the started process instance and drilldown to the waiting user task
6. copy user task id and use postman collection to POST JSON collection with cars
7. The console should now print car name and car types for all cars present in the collection.

Output should be:
```
printing car name:
VW
printing car type:
Golf
printing car name:
Seat
printing car type:
Ibiza
```


