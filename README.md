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

To do it use the following format:
```js
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {},
      "geometry": {
        "coordinates": [
          [
            [
              22.529892879491626,
              6.790980004606666
            ],
            [
              29.763365768917964,
              0.977892637346514
            ],
            [
              33.78561805874617,
              7.542737166575662
            ],
            [
              25.603070278174954,
              10.284504073954949
            ],
            [
              22.529892879491626,
              6.790980004606666
            ]
          ]
        ],
        "type": "Polygon"
      }
    }
  ]
}
```

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
* Submit your solution that we could access it via link, we strongly recommend doing it via GitHub repository
* Cover all edge cases and make sure that your solution works correctly
* Describe how to run your program in terminal. Pass region and location files as input parameters. Example: **scala your-app --regions=regions.json --locations=locations.json --output=results.json**
* Create a README which explains how to compile and run your program.


### Optional requirements:
* Cover your solution by tests (including all edge cases)
* Implement it in scala
* Implement algorithm which will match the location with the corresponding region
