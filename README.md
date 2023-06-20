# internship-task

This is a test assignment for TravelTime internship.

In this test task, your goal is to analyze two provided JSON files - 
one containing region coordinates, the other listing various locations. 
You need to parse these files and create an algorithm that matches the locations to their regions based on the coordinates.
One region can contain multiple locations and one location can match multiple regions.
The result should be a json which contains names of each regions and their corresponding locations.

**Reminder**:

One region can contain multiple polygons. To display provided regions on a map, you can use this website.

### Input files:

Locations:
```js
[
  {
    "name": "<unique identifier>",
    "coordinates": [<longitude>, <latitude>]
  },
  ... // more locations
]
```

Regions:
```js
[
  {
    "name": "<unique identifier>",
    "coordinates": [
      [[<longitude>, <latitude>], [<longitude>, <latitude>]], 
        ... // more polygons    
    ] - array of polygons, where each polygon is an array of coordinates.
  },
  ... // more regions
]
```

### Output files:

Results:
```js
[
  {
    "region": "<region identifier>",
    "matched_locations": [
      "<location identifier>",
      "<location identifier>",
    ]
  },
  ... // more regions
]
```


### Main requirements:
* Submit your solution to github and send us a link to the repository
* Cover all edge cases and make sure that your solution works correctly
* Create a cli command which will take regions and locations files as arguments. Example: **./your-cli-cmd --regions=regions.json --locations=locations.json --output=results.json**
* Create a readme where you'll explain how to run this cli command 


### Optional requirements:
* Cover your solution by tests (including all edge cases)
* Implement it in scala
* Implement algorithm which will match the location with the corresponding region
