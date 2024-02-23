# internship-task

This is a test assignment for Scala TravelTime internship.

For this test task your goal is to match locations to their appropriate regions. 
Each location has a coordinate. You have to find which locations fit into given regions by their coordinates. 
A single region can contain multiple locations. A single location can appear in multiple regions, thus meaning regions can overlap with each other.
Locations and regions are provided in separate JSON files. You will have to parse these files to read locations and regions data. 

After you successfully parsed JSON files you will need to create an algorithm or use third party library that matches locations to their regions based on their coordinates.
The result of your task should be a JSON file which list all of the regions with their coresponding locations.


**Reminder**:

One region can contain multiple polygons. To display coordinates of provided regions on a map, you can use this website https://geojson.io/. 

### Input files:

[Locations](input/locations.json):
```js
[
  {
    "name": "<unique identifier>",
    "coordinates": [<longitude>, <latitude>]
  },
  ... // more locations
]
```

[Regions](input/regions.json):
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

[Results](output/results.json):
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
* Submit your solution that we could access, you should do it via GitHub repository. If you are not writing your solution in Scala or Java, it would be convenient for us if you send an additional link to replit.com with your solution. Replit is an online IDE and hosting platform, if you submit the code there we won't have to try to run C# on Linux.
* Cover all edge cases and make sure that your solution works correctly
* Describe how to run your program in terminal. Pass region and location files as input parameters. Example: **scala your-app --regions=regions.json --locations=locations.json --output=results.json**
* Create a README which explains how to compile and run your program
* Cover your solution by tests (including all edge cases)


### Optional requirements:
* Implement it in scala
* Implement algorithm which will match the location with the corresponding region
